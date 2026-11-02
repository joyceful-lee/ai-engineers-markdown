# Iterate It

Just because an AI generated your site does not mean you are done. We still need to test if the core functions of the site work.

## Test It

Before you start hunting for random bugs, go through the process of using the site.

1. Sign up, create a group, and start a project.
2. Invite a second account and create a task with an assignee, deadline, and status.
3. Log in as the assignee, update the task, and check that project progress changes.
4. Try to assign tasks as a member and see if it's accepted.
5. Refresh or log out and back in to check that tasks and roles remain saved.
6. Open the project from an account outside the group and confirm that access is blocked.

Some tests to look out for include:

- Can a task be assigned only to someone who belongs to the correct group?
- Can contributors change deadlines or settings that belong to managers?
- What happens to access and assignments when a member is removed or their role changes?
- Does deleting a task update progress?

## Fix It

As you test your site, record issues that need fixing. When noting an issue, include:

- When or where the problem occurs
- What currently happens (the issue)
- What should happen instead (the fix)

Send Codex the issue and the change you want, then repeat the flow to check that the fix works.

```prompt
Review this project and return a changelog of the work done so far.

Requirements:
- Count how many distinct iterations or change rounds you can identify from the conversation and the current code.
- Start with one line: "Iterations so far: N"
- Then give a bullet list changelog. Each bullet should describe one meaningful change in plain language.
- Be honest about the count. If there are fewer than 10 clear iterations, say so.
```

## Let's think about it

What iterations did you make to your website since you first generated it? Use the prompt above to get the changelog. You must have made at least 3 changes to your website.

Upload a screenshot of your updated website.
