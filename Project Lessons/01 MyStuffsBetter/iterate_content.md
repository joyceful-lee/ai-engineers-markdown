# Iterate It

Just because an AI generated your site does not mean you are done. We still need to test if the core functions of the site work.

## Test It

Before you start hunting for random bugs, go through the process of using the site.

1. Sign up and create a collection
2. Add several cards, including one with an image.
3. Edit a card, remove another, and refresh the page to check that your changes were saved.
4. Make a collection public.
5. From a second account, open the public collection and subscribe to it.
6. From the collection owner's account, add another card, then check for an update in the subscriber's account.
7. Sign out.

Some tests to look out for include:

- Do changes stay after refreshing page or logging out?
- Are private collections blocked for visitors and accounts without permissions?
- Can user view public collections without being able to edit or delete someone else's cards?
- What happens to subscribers when the owner deletes a collection?
- Does the site explain upload or submission errors?

## Fix It

As you test your site, record issues that need fixing. When noting an issue, include:

- When or where the problem occurs
- What currently happens (the issue)
- What should happen instead (the fix)

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

Upload a screenshot of your newly generated website.
