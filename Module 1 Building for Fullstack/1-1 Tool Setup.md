# Tool Setup

Welcome to AI Engineers! In this lesson, we’ll set up the tools we’ll need to create the full-stack applications. If you already have Codex or Qoder installed from another course, you can create a new Codex project and jump ahead to step 2.

You'll be using:

1. **Codex or Qoder:** an AI coding tool that helps create and improve your apps
2. **Bun:** a JavaScript runtime that runs development tools and local servers
3. **Neon:** a site to host your database and authentication

## 1. Choose an AI Tool

Codex and Qoder are AI coding assistants that we'll use to create files, change code, and help run our applications. Codex is made by OpenAI, the same people who make ChatGPT, and it grants you access to a specialized version of ChatGPT for coding. Qoder is an alternative to Codex that can be used by any students who cannot access Codex for various reasons, including restrictions from living in foreign countries, or issues regarding an OpenAI account.

### Codex

If you're using Codex, we recommend using your own ChatGPT account; however, if you don't have one, open the [Minddo student dashboard](https://minddo.ai/dashboard) choose **Get a Key** from the navigation bar on the left-side, and generate a temporary API key to log into Codex with.

Temporary keys expire, so you'll need to create a new one at the start of each class. After signing in with a temporary key, students must select **5.6 Luna** as the model in Codex.

* The **Get a Key** section includes step-by-step instructions with screenshots for signing into Codex with the temporary API key.  

**NOTE:** Temporary keys only work with 5.6 Luna and are not compatible with other Codex models.

**Tips:**

* If sign-in fails, check VPN, browser pop-ups, and that your OpenAI account has access to Codex.

### Qoder

[Qoder](https://qoder.com/) has a slightly different interface than Codex but functions similarly. You can download Qoder [from here](https://qoder.com/en/download).

**NOTE:** We also ask that students use their own Gmail account to sign up for Qoder. Signing up for Qoder grants access to a 2-week long Pro trial without need for a credit card or other authentication means.

After the trial, the student will be responsible for maintaining a subscription.

**NOTE:**

While this course commonly uses "Codex", it is generally interchangeable with whichever AI tool you end up using. If a student is using Qoder, for instance, any instruction referring to Codex should be done with Qoder instead.

### Let’s think about it

* [ ] Install the OpenAI Codex application and create a new project.

## 2. Bun Installation

Bun is an all-in-one JavaScript runtime, basically a toolkit for programming with JavaScript. It gives us to commands we need to start a local server and run our web apps!

### Steps

1. Install **Bun** using the official installer for your OS (see [bun.sh](http://bun.sh) for current steps).  
2. Open a terminal.
3. Run `bun --version` to verify installation.  
4. If it is successfully installed, a version number should appear.

### Tips

* If your terminal doesn't find `bun`, restart the terminal or add the install path to your `PATH` as the installer prints.  
* Bun aims to be a drop-in replacement for many Node workflows; you will use it alongside Codex in the next lesson.

### Let’s think about it

* [ ] Bun is installed
* [ ] `bun --version` prints a version

## 3. Neon Connection

[Neon](https://neon.com/?gad_source=1&gad_campaignid=21329093217&gclid=CjwKCAjwxeHWBhBPEiwAiqtQ-XhX2xTB3lHQ-gUr2AV8IJcMDmL8t2ZJ4c6MjUMNg4XCxF22S9p30xoC6y0QAvD_BwE) is what we’ll be using to host our databases and manage authentication (users for our sites).

These steps will connect Codex to Neon, but we'll still need to define the tables and features later.

### Steps

1. Create a Neon account.  
2. Make sure the Codex project you created is open.
3. Connect Neon with Codex by copy-pasting the following set-up prompt: [message.txt](https://drive.google.com/open?id=1MILicu9O0WlM_XQgRbr0EcMbx7M8WjYY) into Codex.
4. Complete the Neon sign-in and authorization, if requested.  
5. Wait for Codex to verify that it can access the correct project and database.

### Let’s think about it

* [ ] Open the Neon Console and confirm that the same project appears.
