# File Storage and Security

Your current Social Feed app should let users:

1. Create accounts  
2. Write posts  
3. Leave comments

Up next, we’ll be introducing **storage** and how images and other files can be connected to posts before finishing the app with a final security audit.

You will:

1. Set up File Storage
2. Add Image Uploads  
3. Security Audit

## 1. Set up File Storage

Our app will store two kinds of information: **post and comment details** and **image files**.

We’re currently using **Neon Postgres** to store the information for each post, comment, and author (tables); however, we’ll be using **Vercel Blob** to store the uploaded images.

Before creating a Blob store, deploy or connect your social feed project to Vercel. You can view storage by navigating from the `Vercel Dashboard > Storage`.

```prompt
Deploy this project to Vercel under the name, [desired name], using Neon for the database and authentication (Neon Better Auth using email/password).

Inspect the app first, then create or connect the GitHub repository, Neon project, and Vercel project. Configure the database connection, apply the required schema migrations, and store credentials securely in Vercel environment variables. Keep secrets out of Git.

Run the build and relevant tests, deploy to production, and verify that the live app can read and write to Neon. Set up automatic deployments from GitHub.

Complete routine setup without asking for confirmation. Ask before deleting data, overwriting existing resources, or enabling paid services. Finish with the live URL, repository link, and any remaining setup.
```

Vercel Blob uses a **store** to hold files. Each uploaded file is called a **blob** and has a pathname that identifies it. For our app, we’ll create a private Blob store called `post-images`.

In our post’s database row, it should store the file reference, not the entire image.

To manually create a blob, you can follow the steps below:

1. Create the store from the Vercel project’s **Storage** tab.
2. Choose **Create Database > Blob**, **Private**, and select the environments you will use.
3. Make sure to check `Add a read-write token env var to this connection`

The required Environment Variables will be added automatically.

```text  
Configure private Vercel Blob storage for this app using a Blob store called `post-images`.

Allow jpg, png, webp, gif. Max file size: 5MB.  
Set permissions so only authenticated users can upload and only the owner can access, replace, or remove an image.
Store image metadata and ownership in the verified Neon Postgres project.
Handle upload or database failures without leaving broken references.
```

### Let’s think about it

- [ ] Confirm the post-images store appears in Vercel Blob  
- [ ] Attempt an upload while signed out and confirm the backend rejects it.

## 2. Add Image Uploads

Although Vercel Blob is now configured, our app does not have the capability to handle it yet. We need to ensure that users can optionally attach an image to a post and it will successfully add the image to the store and display it.

```text  
Add image upload to the post creation form in this social feed app.

Requirements:  
- Add a file input to the post form  
- Upload the image to the private Vercel Blob store named `post-images`
- Add an optional text column for the image pathname to the existing `posts` table without deleting existing data.
- Store the resulting Blob pathname on the post row as `imageId`  
- Store the image owner and metadata in Neon Postgres, not the image binary.
- Images are optional — submitting a post without an image should still work  
- Only authenticated users may upload, and only the post author may view, replace, or remove its attachment.
- Verify file type, file size, and ownership on the server.

Keep the upload flow simple.  
```

### Let’s think about it

- [ ] Submit one post with an image and one without, verify that `imageId` is set or empty accordingly.

## 3. Security Audit

An **audit** checks whether our app meets its requirements and looks for security weaknesses that may exist. It helps us find problems, such as users being able to edit someone else’s posts or upload files they shouldn’t be allowed to.

```text  
Perform a security analysis of this social site app.

Check:  
- Can a non-logged-in visitor create posts or comments?  
- Can one logged-in user edit or delete another user's post?  
- Are Neon’s table permissions set correctly for each role?  
- Are there any API routes or server actions that trust the client without validation?

Report every issue you find. For each issue, explain the risk and suggest the fix.  
```

```text  
Apply the security fixes you identified.

Requirements:  
- Anyone can read posts and comments  
- Only logged-in users can create posts and comments  
- Only the post/comment author can edit or delete their own content  
- Profiles can be read by anyone, but only edited by the owner

Use Neon table permissions and row-level permissions.  
Also validate ownership server-side — don't trust the client alone.  
```

### Let’s think about it

- Describe one error the security analysis outlined. If no issue is reported, explain one data protection added to your site.
