# Data Models and CRUD

In Module 1, we built a TODO app that saved data in a database. In this module, we’ll cover the concepts for those features by creating a Reddit-style social feed app. In Codex, create a new project called "Social Feed", so we can keep this project separate from our TODO app. Before creating tables, follow the Neon setup procedure from Module 1 in this workspace as well.

To create the site, we’re going to start with the following steps:

1. Create a Mockup
2. Define the Data Model  
3. Understand CRUD  
4. Wire Up Posts

## 1. Build a Mockup

A **mockup** is a static visual representation of an application’s intended look and feel (e.g., layout, colors, typography, button styles, etc.). Once navigation or page interactions are added, it becomes an **interactive prototype**.

By starting with a mockup or interactive prototype, it helps us see how the app will look and how our users may navigate it before connecting it to a database or building the backend. We can fix confusing layouts, test navigation, and make adjustments while the app is still easy to change!

For our social feed app, we want to generate a stripped-back static version of the site with hardcoded posts and comments.

```text
Generate a stripped-back static Next.js app that looks like a Reddit-style social media site.

Include:  
- A feed page showing posts with title, author, vote count, and comment count  
- A post detail page showing the full post content and a list of comments  
- A simple navbar with the site name  
- A sidebar with community/topic links (hardcoded)

No backend, no database — use hardcoded mock data. Tailwind CSS for styling.  
Keep it clean and minimal. No auth, no forms that actually submit.
```

### Tips

* Walk through every page before moving on — note what the feed, post detail, and sidebar should look like when data is real.  
* Keep field names from the mockup in mind; the next section defines the official data models.

### Let's think about it

* Submit a screenshot of your static social feed app running locally in the browser

## 2. Define the Data Model

A **data model** describes what information an application stores, how it is organized, and how different records relate to one another. You can think of it as a blueprint for your app’s data!

In Neon, a **table** groups similar records.

* Each **row** is one record  
* Each **column** is a field  
  * A field’s **data type** defines what kind of value a field can store

Data Types

| PostgreSQL | Meaning | Used for |
| :--- | :--- | :--- |
| text | text/string | titles, post content, display names |
| integer | whole number | vote counts |
| boolean | true/false | task completion |
| timestamptz | date and time | creation time |
| uuid (or integer key) | unique identifier | identifyng records |

If `posts.id` is an integer, the related `comments.postId` field should also be an integer. Similarly, if post Id's use uuids, the matching comment field should use uuids as well.

For our social feed app, the following data models can be used:

### Posts

| Field | Type | Notes |
| :---- | :---- | :---- |
| id | integer | Unique, required |
| title | text | Required |
| content | text | The post body |
| authorId | text | Links to the user |
| voteCount | integer | Starts at 0 |
| createdAt | timestamptz | Defaults to the current date and time |

### Comments

| Field | Type | Notes |
| :---- | :---- | :---- |
| id | integer | Unique, required |
| postId | integer | Which post this comment belongs to |
| content | text | The comment body |
| authorId | text | Links to the user |
| createdAt | timestamptz | Defaults to the current date and time |

### Users

| Field | Type | Notes |
| :---- | :---- | :---- |
| userId | text | User ID created with Neon's Better Auth |
| displayName | text | Shown on posts |
| bio | text | Optional |
| createdAt | timestamptz | Defaults to the current date and time |

A post can have many comments with each comment identifying its post through the `postId`. Posts and comments link to the author through `authorId`.

Send this prompt in to create the tables in Neon:

```text
Create the following tables in Neon:

1. ‘Post’ table with fields: id, title, content, authorId, voteCount, createdAt  
2. ‘Comment’ table with fields: id, postId, content, authorId, createdAt  
3. ‘Profile’ table with fields: userId, displayName, bio, createdAt

Use stable IDs, appropriate types, and relationships.  
A post can have many comments with each comment identifying its post through the `postId`. Posts and comments link to the author through `authorId`.
```

### Let's think about it

* Explain how the app finds a post’s comments and their authors.  
* Upload a screenshot of one of the tables in Neon.

## 3. Understand CRUD

**CRUD** stands for Create, Read, Update, and Delete.

For our app, the operations will follow:

| Operation | In this app |
| :---- | :---- |
| Create | Submit a new post or comment |
| Read | Load the feed or a post with its comments |
| Update | Edit a post or comment |
| Delete | Remove a post or comment |

### Let's think about it

* “Changing the title of a post” falls under which one of the operations?

## 4. Wire Up Posts

Now it’s time to connect the mockup’s hardcoded data with real records!

```text  
Using the tables created (post, comment) and the existing mockup app, build [Next.js](http://Next.js) pages that:  
- List all posts on the feed page (replace mock data with real Neon data)  
- Show a single post with its comments on the detail page  
- Let a user create a new post via a form  
- Let a user add a comment to a post via a form

Keep it minimal — basic forms, no auth yet.  
Create a clearly labeled development fixture profile for the
temporary author, consistent with the schema's relationships.
Use it only during local development. Replace the fixture identity
when real authentication is added 
```

### Tips

* After creating a post, open the Neon console and confirm the row exists before trusting the UI.  
* If the feed is empty, check table names, selected database connections, and access policies.

### Let's think about it

* [ ] The feed loads posts from Neon db, not mock data  
* [ ] Creating a post adds real data in Neon  
* [ ] The post detail page loads the correct post and its comments
