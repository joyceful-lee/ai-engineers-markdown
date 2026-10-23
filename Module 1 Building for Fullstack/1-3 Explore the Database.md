# Explore the Database

If you completed AI Native, you may be wondering what the difference between the TODO App in Lesson 2 and the Hard Workers Arcade is. They both allow us to create a to-do list in our browser, so why are we doing it again?

The main difference between the two projects is the use of **databases.** A database stores organized information that an application can retrieve and update.

Databases have:

* **Table**: groups related information together.
* **Row**: is one record in a table (in our task table, a row would be one task)
* **Column**: stores one kind of information about each record (e.g., title, completion status, difficulty)

Table example:

| id | title | completed |
| :--- | :--- | :--- |
| 001 | Finish essay | false |

For Hard Workers Arcade, we used `localStorage` to save our to-do lists on our browser. This allows us to save our lists on a page refresh; however, if we use a different computer (or even a different browser), our saved list won’t appear!

For our TODO App, we'll use a Neon database to store our to-do list online. When we sign in to the same account from another browser or computer, the app will retrieve our saved tasks from the database by using our account's `userId` to find the tasks that belong to us!

## Navigating Neon

In Lesson 1, you should’ve opened the Neon Console to see the project that is connected to your Codex app.

You can view your existing table by:

1. Click on your project  
2. Open up the “Postgres database” category in the left navbar  
3. Open `Tables`

To see how the database works, you can test the following:

1. Create a task called “Find this task”  
2. Refresh the Neon table view and find its row.  
3. Update the title through your app.  
4. Refresh the table view again to see the change.
5. Delete the task through your app and confirm the row disappears.

## Let’s think about it

* [ ] Submit a screenshot of your database tables in Neon.
