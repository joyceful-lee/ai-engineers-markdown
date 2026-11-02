# Expand It

River can now find saved recipes and get suggestions for what to cook. Her friend Maya tries the site too.

```talker
{
name: Maya
bubble: speech
face: 🧑
}
I tried a few different ingredients, but there aren't many matching recipes saved yet. Could the site find ideas from somewhere else too?
```

Great idea, Maya! Recipe recommendations currently rely on recipes added by users, so the selection is limited while the site is new. Connecting an external recipe API would offer more ideas while preserving the existing collection and recommendation features.

## External APIs

An **API**, or application programming interface, lets one application request information from another. A recipe API can provide recipes, ingredient lists, pictures, and source links that are not already in your database.

Your site sends a request containing a search or selected ingredients, receives structured data, and turns that data into something a cook can use. The response may contain missing information, no matches, or an error, so the site needs to handle each case.

Some APIs require a secret key. Keep that key on the server rather than in browser code or GitHub. Recipes supplied by another service should show their source, and the API's rules determine which images and details may be displayed or saved.

## Example

Maya searches for recipes using mushrooms. The site shows recommendations from its own collection and a separate set of results from the recipe API. Each external result includes its source and a link to the original recipe. If the service is unavailable, Maya sees a helpful message and can still use the recipes saved on the site.

## New Goal

Connect an external recipe API to help users discover more meals without losing access to the site's own recipes and recommendations.

For our sample project, we used [TheMealDB](https://www.themealdb.com/api.php), but other free APIs can be found [here](https://github.com/public-apis/public-apis#food--drink).

```checklist
{
title: Updated Project Requirements
color: #e7f7dc
}
- Connect an external recipe API to find ideas using searches or selected ingredients.
- Let users review, edit, and save external recipes to their own collection.
- Follow the API’s rules for using recipe details and images, protect secret keys, and validate requests and responses server-side.
- Clearly explain loading, missing details, empty results, and errors while preserving the user’s search.
- Keep existing recipes, recommendations, and community features working when the API is unavailable.
```

## Let's think about it

What information comes from the external API, and how can someone keep using your site if that service is unavailable?
