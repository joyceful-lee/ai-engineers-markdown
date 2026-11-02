# Iterate It

Just because an AI generated your site does not mean you are done. We still need to test if the core functions of the site work.

## Test It

Before you start hunting for random bugs, go through the process of using the site.

1. Sign up and open the map or world.
2. Enter an available location and complete its challenge.
3. Open the newly unlocked location, then refresh during an unfinished challenge.
4. Log out and back in to check that location progress is preserved.

Some tests to look out for include:

- Are locked locations blocked until their requirements are complete?
- Does refreshing or returning later preserve the correct challenge state?
- Can you repeat a completed challenge?
- Does a failed save preserve the player's progress and provide a way to retry?

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
