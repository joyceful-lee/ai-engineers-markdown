# Iterate It

Just because an AI generated your site does not mean you are done. We still need to test if the core functions of the site work.

## Test It

Before you start hunting for random bugs, go through the process of using the site.

1. Open the builder without signing in.
2. Choose a tea base, milk, ice level, and several toppings.
3. Go back to change an earlier choice and check the preview, selections, and total.
4. Remove a topping, review the finished drink, and submit the order.
5. Read the order card or code as if you were preparing the drink.

Some tests to look out for include:

- Can a new visitor tell within a few seconds that this is a custom boba drink builder?
- Can you pick tea type and control how much tea goes in the cup?
- Can you pick milk type and control how much milk goes in the cup?
- Can you set an ice level and add multiple toppings to the same drink?
- Does the drink summary update as you build and show the full order clearly at the end?
- Can you finish with an order summary or code you could show at a register?
- Does saved drink data persist in Neon, not just in the browser?

After completing Expand It, create a completed order and an unfinished builder session, then check the staff dashboard for the same date range. Also test repeated step visits, a date range with no activity, and access from a signed-out visitor or non-staff account. The dashboard should count activity accurately and block unauthorized access.

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
