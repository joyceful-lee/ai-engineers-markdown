# Iterate It

Just because an AI generated your site does not mean you are done. We still need to test if the core functions of the site work.

## Test It

Before you start hunting for random bugs, go through the process of using the site.

1. Sign up and create a recipe with ingredients, steps, preparation time, tags, and a picture.
2. Add a second recipe without a picture, then edit the first recipe.
3. Refresh the page and search for the recipe using a tag or time filter.
4. From a second account, like the recipe and leave a comment.
5. Choose a cooking goal and check the recipe suggestions and their explanations.
6. Sign out and check what a visitor can read and which actions require an account.

Some tests to look out for include:

- Do recipes, pictures, likes, and comments remain after refreshing or logging back in?
- Can users edit or delete someone else's recipe or comment?
- What happens when a search or recommendation has no matches?
- Do recommendations respect the selected time and tags, with an explanation that matches the recipe?
- What happens to likes and comments when their recipe is deleted?

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
