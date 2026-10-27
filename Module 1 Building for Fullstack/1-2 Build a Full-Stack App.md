# Build a Full-Stack App

In this lesson, you will build a **TODO App** in your browser using Codex.

You will:

1. Open your project in Codex  
2. Plan and send your prompt  
3. Build and test your app
4. Deploy your app

## 1. Open your project in Codex

As a reminder, a **project** is a workspace where the AI keeps your files and conversations in one place.

### Open Your Project

In Lesson 1, you should’ve created a new project in Codex.

1. In Codex, go to the **Projects** section in the left sidebar.  
2. Locate project you created in Lesson 1.  
3. Give the project a short name you will recognize, such as **My TODO App**.

You're ready once Codex's chat screen mentions your project's name, such as "What should we build in XXXX?".

### Let’s think about it

- [ ] Check that a new project was created.

## 2. Plan and send your prompt

Before we ask Codex to build anything, we need to plan what our app will do. The core requirements for the TODO App are outlined below.

### Project Requirements

- Add, read, update, and delete tasks from the task list.  
- Be able to create an account, sign in, and sign out with Neon authentication.  
- Save tasks in Neon, so they persist after log out.  
- Sync tasks with Neon whenever a task is added or changed
- Ensure users can only edit and access their own tasks.

Think about:

- What information should each task have?  
- What happens after someone adds a task?  
- What does the user see if they have no tasks?

Use this prompt as a guide. Replace the brackets with your own ideas.

```text
Build a TODO app in this existing workspace.

Audience and goal:
[Who will use the app, and what should it help them accomplish?]

Task information:
[What information should each task contain?]

User flow:
[What should a user see first? How do they add, edit, complete, and delete a task?]

Empty state:
[What should someone see before they add any tasks?]

Accounts and data:
- use Neon Better Auth for email/password sign up and login.
- Save tasks in the verified Neon project for this workspace
- Users must be able to return and retrieve their saved tasks
- Users can access and read, create, update, and delete only their own tasks.
- Guests cannot access task records.

Do not create a duplicate Neon project.
```

### Let’s think about it

- Submit a screenshot of your TODO web app running locally in the browser.  
- In 2–4 sentences, describe how you prompted Codex to create the app.

## 3. Test your app

After Codex finishes generating your site, it may open a version of your website using ChatGPT Sites. We **do not** want this. Ask Codex to run a version locally using bun.

```prompt
Start my TODO app locally using Bun.
```

You can also run it manually by navigating to your current working directory in command prompt or powershell using:

```command
cd \path\to\directory
bun --bun run dev
```

Ctrl+click the local host link to open up a preview of your site (it may take a moment to load the first time).

Take a few minutes to explore the site and test all the features available. Make note of features that don’t work, layouts that need altering, and any other note that you want improved.

A solid way to test is to follow the sequence to add a task:

1. Add Task
2. Edit Task
3. Complete Task
4. Refresh Page
5. Sign Out
6. Sign Back In
7. Delete Task

Afterwards, send the appropriate prompts into Codex to improve your site.

### Let’s think about it

- List three things you’ve improved upon in your website

## 4. Deploy Your Site

To publish our sites, we are using **Vercel**. Vercel is a platform that helps us host and deploy (publish) more advanced websites and applications through using our repositories on GitHub.

The first step is to push your project to GitHub in a new repository. If the project isn't uploaded to GitHub yet, you can use the prompt below.

```prompt
Push the current project to a new public GitHub repository with the same name under my account.

Inspect the folder and existing Git setup first. Add an appropriate .gitignore so secrets, environment files, dependencies, and build outputs stay out of Git. Commit the project, create the repository, and push it with main as the default branch.

Preserve existing files and Git history. Complete routine steps without asking for confirmation, and finish with the repository link.
```

After the GitHub repository is created, you can connect it to Vercel!

```prompt
Deploy this project to Vercel under the same name, using Neon for the database and authentication (email/password).

Inspect the app first, then create or connect the GitHub repository, Neon project, and Vercel project. Configure the database connection, apply the required schema migrations, and store credentials securely in Vercel environment variables. Keep secrets out of Git.

Run the build and relevant tests, deploy to production, and verify that the live app can read and write to Neon. Set up automatic deployments from GitHub.

Complete routine setup without asking for confirmation. Ask before deleting data, overwriting existing resources, or enabling paid services. Finish with the live URL, repository link, and any remaining setup.
```

You can also do it manually by following the steps below:

1. Confirm your project is on GitHub
2. Go to [Vercel](vercel.com/new)
3. Sign in with GitHub and import your project using these settings:
   - Framework: `Next.js`
   - Production branch: `main`
   - Root directory: `.`
4. Add the following Environment Variable for all environments (Production, Preview, Development) or use Neon integration:
   - `DATABASE_URL`:`Neon > Connect > Postgres database > Connection String
   - `NEON_AUTH_BASE_URL`: Neon > Connect > Auth > Auth URL
5. Click **Deploy**

### Add image storage

If your app supports images, send the prompt or follow the steps below:

```prompt
Create a Vercel Blob store named [store name] and connect it to my current project linked to Vercel.

Use private access. Configure the required credentials securely for local development and Vercel deployments, keeping secrets out of Git. Verify the connection with a small test upload, then report the store name and any remaining setup.

Preserve existing resources and ask before enabling paid services.
```

Manual Steps:

1. Open the Vercel dashboard and click `Storage` in the left navbar.
2. Click `Create Storage > Blob`.
   - Check `Private`.
3. Check the `Add a read-write token env var to this connection` at the bottom.
4. Create the Blob.
   - Double-check that `BLOB_READ_WRITE_TOKEN` is now an Environment Variable

**NOTE:** The required environment variables (`BLOB_READ_WRITE_TOKEN`) for the Blob should be automatically added.

The project link can now be found in your GitHub repository in the `About` section or the `Domain` section of Vercel.
