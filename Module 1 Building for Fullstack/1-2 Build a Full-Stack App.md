# Build a Full-Stack App

In today’s lesson, you will build a **TODO App** in your browser using Codex.

You’ll do the Following

1. Open your project in Codex  
2. Plan and send your prompt  
3. Test your site

## 1. Open your project in Codex

As a reminder, a **project** is a workspace where the AI keeps your files and conversation in one place.

### Open Your Project

In Lesson 1, you should’ve created a new project in Codex.

1. In Codex, go to the "Projects" section in the left sidebar.  
2. Locate project you created in Lesson 1.  
3. Give the project a short name you will recognize, such as "My TODO App" or "TODO App Project".

You're ready once Codex's chat screen mentions your project's name, such as "What should we build in XXXX?".

### Let’s think about it

- [ ] Check that a new project was created.

## 2. Plan and send your prompt

Before we ask Codex to build anything, we need to plan what our app will do. The core requirements for the TODO App are outlined below.

Project Requirements

- Add, read, update, and delete tasks from the task list.  
- Be able to create an account, sign in, and sign out with Neon authentication.  
- Save tasks in Neon, so they persist after log out.  
- Sync tasks from the site to neon after any change.
- Ensure users can only edit and access their own tasks.
- Ensure the site is publicly accessible.

Think about:

- What information should each task have?  
- What happens after someone adds a task?  
- What does the user see if they have no tasks?

You can use this prompt as a guide.

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

## 3. Test your site

After Codex finishes generating your site, it should either open it to the side or provide a link where you can see it.

You can also navigate to your current working directory in command prompt or powershell using:

```command
cd \path\to\directory
bun --bun run dev
```

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

## 3. Deploy Your Site

To publish our sites, we are using **Vercel**. Vercel is a platform that helps us host and deploy more advanced websites and applications.

1. Push your project to GitHub
2. Go to [Vercel](vercel.com/new)
3. Sign in with GitHub and import your project using these setting:
   - Framework: Next.js
   - Production branch: main
   - Root directoy: .
4. Add the following Environment Variable for all environments (Production, Preview, Development) or use Neon integration:
   - DATABASE_URL: `Neon > Connect > Postgres database > Connection String`
   - NEON_AUTH_BASE_URL: `Neon > Connect > Auth > Auth URL`
5. Click Deploy

In order to add images, follow the steps below:

1. Open Vercel and click `Storage` in the left navbar
2. Blick `Create Storage > Blob`
   - If just for images, access can be public.
3. Check the `Add a read-write token env var to this connection`
4. Create the Blob.

The required environment variables for the Blob will be automatically added.

The project link can now be found in your GitHub repository in the `About` section or the `Domain` section of Vercel.
