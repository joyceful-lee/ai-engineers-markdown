# Tool Setup

Welcome to AI Engineers! In this lesson, we’ll set up the tools we’ll need to create the full-stack applications. If you already have Codex or Qoder installed from another course, you can create a new Codex project and jump ahead to step 2.

Tools needed for this course:

1. **AI Tool:** Codex or Qoder - helps write code
2. **Bun** - runs development tools
3. **Neon** - provides database and backend services

[AI Engineers \| Installing Codex Video](https://www.youtube.com/watch?v=34e6ku9RBCg)

## 1. AI Tool Installation

Codex and Qoder are AI coding assistants that can create files, change code, and help you run your application. Codex is made by OpenAI, the same people who make ChatGPT, and it grants you access to a specialized version of ChatGPT for coding. Qoder is an alternative to Codex that can be used by any students who cannot access Codex for various reasons, including restrictions from living in foreign countries, or issues regarding an OpenAI account.

### Codex

**We heavily recommend that students get their own ChatGPT account for this course when using Codex.**

However, for students without a ChatGPT account, they can sign in to the [Minddo student dashboard](https://minddo.ai/dashboard), open the **Get a Key** section, and generate a temporary API key to log into Codex with.

* The **Get a Key** section includes step-by-step instructions with screenshots for signing into Codex with the temporary API key.  
* After signing in with a temporary key, students must select **5.6 Luna** as the model in Codex. Temporary keys only work with 5.6 Luna and are not compatible with other Codex models. The **Get a Key** section shows how to open the model picker and choose Luna.  
* Keys are short-lived and are revoked automatically after the time shown on the dashboard.  
* Students should generate a new key at the start of each class session and cannot reuse an expired key.

**NOTE:** A generated key is NOT necessary for any student not using Codex (e.g. Qoder) or those with an existing OpenAI/Codex subscription. These students do not require keys to participate in class.

**Tips:**

* Keep Codex updated; the first-run experience changes as the product ships new features.  
* If sign-in fails, check VPN, browser pop-ups, and that your OpenAI account has access to Codex.

### Qoder

[Qoder](https://qoder.com/) has a slightly different interface than Codex but functions similarly.

You can download Qoder [from here](https://qoder.com/en/download).

**NOTE:** We also ask that students use their own Gmail account to sign up for Qoder. Signing up for Qoder grants access to a 2-week long Pro trial without need for a credit card or other authentication means.

### Note on "Codex" in this course

While this course commonly uses Codex, it is generally interchangeable with whichever AI tool the student ends up using. If a student is using Qoder, for instance, any instruction referring to Codex should be done with Qoder instead.

### Let’s think about it

* [ ] Install the OpenAI Codex application and create a new project.

## 2. Bun Installation

Bun is an all-in-one JavaScript runtime, basically a toolkit for programming with JavaScript. We’re going to install it and run it from a terminal so we can execute scripts and local servers the same way the video and Codex expect.

[AI Engineers \| Bun Installation](https://www.youtube.com/watch?v=5xkaBvt4NXk)

### Steps

1. Install **Bun** using the official installer for your OS (see [bun.sh](http://bun.sh) for current steps).  
2. Open a terminal and verify the install with a version command (e.g. `bun --version`).  
3. Optionally run a one-line script or `bun init` in a test folder to confirm Bun executes.

### Tips

* If your shell does not find `bun`, restart the terminal or add the install path to your `PATH` as the installer prints.  
* Bun aims to be a drop-in replacement for many Node workflows; you will use it alongside Codex in the next lesson.

### Let’s think about it

* [ ] Install the Bun JavaScript runtime on your machine  
* [ ] Run Bun from a terminal (e.g. `bun --version`) and confirm it prints a version

## 3. Neon Connection

[Neon](https://neon.com/?gad_source=1&gad_campaignid=21329093217&gclid=CjwKCAjwxeHWBhBPEiwAiqtQ-XhX2xTB3lHQ-gUr2AV8IJcMDmL8t2ZJ4c6MjUMNg4XCxF22S9p30xoC6y0QAvD_BwE) is what we’ll be using to host our databases and control authentication.

These steps will connect Codex to Neon, but we'll still need to define the tables, code, and authentication.

### Steps

1. Create an account with Neon.  
2. Make sure the Codex project you created is open  
3. Connect Neon with Codex by copy-pasting the following set-up prompt: [message.txt](https://drive.google.com/open?id=1MILicu9O0WlM_XQgRbr0EcMbx7M8WjYY)  
4. Complete the Neon sign-in and authorization, if requested.  
5. Wait for Codex to verify that it can access the correct project and database.

### Let’s think about it

* [ ] Open the Neon Console and confirm that the same project appears.
