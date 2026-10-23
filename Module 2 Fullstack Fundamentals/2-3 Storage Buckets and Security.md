# Storage Buckets and Security

Our current app should let users:

1. Create accounts  
2. Write posts  
3. Leave comments

Up next, we’ll be introducing **storage** and how images and other files can be connected to posts before finishing the app with a final security audit.

1. Storage Buckets  
2. Add Image Uploads  
3. Security Audit

## 1. Storage Buckets

Our app will store two kinds of information: **post and comment details** and **image files**.

We’re currently using **Neon Postgres** to store the information for each post, comment, and author; however, we’ll be using **Neon Object Storage** to store the uploaded images.

You can view object storage by navigating from the `Neon Console > Object storage`.

Inside of object storage, we can create **buckets**. A bucket is a named container for files (similar to how a folder works). For our app, we’ll create a bucket called `post-images` to hold our images. In the bucket, each object will have an **object key** that will be used to identify which object should be used.

In our post’s database row, the object key is used instead of the actual image or file.

Use the following prompt to create a bucket:

```text  
Configure Neon Object Storage for this app using the verified project and branch. Create or reuse a storage bucket called `post-images`.

Allow jpg, png, webp, gif. Max file size: 5MB.  
Set permissions so only authenticated users can upload.
Handle upload or database failures without leaving broken references.
```

### Let’s think about it

- [ ] Confirm the post-images bucket appears in Neon Object storage  
- [ ] Attempt an upload while signed out and confirm the backend rejects it.

## 2. Add Image Uploads

Although Neon is now wired to accept images, our app does not have the capability to handle it yet. We need to ensure that users can optionally attach an image to a post and it will successfully add the image to the bucket and display it.

```text  
Add image upload to the post creation form in this social feed app.

Requirements:  
- Add a file input to the post form  
- Upload the image to the Neon’s `post-images` bucket  
- Add an option text column for the image refence to the existing `posts` table without deleting existing data.
- Store the resulting object key on the post row as `imageId`  
- Images are optional — submitting a post without an image should still work  
- Only authenticated users may upload, and only the post author may replace or remove its attachment.

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
