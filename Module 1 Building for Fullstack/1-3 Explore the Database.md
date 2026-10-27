# Explore the Database

If you completed AI Native, you may be wondering what the difference is between the **TODO App** and the **Hard Workers Arcade**. They both create tasks or todo lists, so why did we do it again?

The main difference between the two projects is how the information is stored.

For Hard Workers Arcade, we used `localStorage` to save our to-do lists on our browser. This allows us to save our lists on a page refresh; however, if we use a different computer (or even a different browser), our saved list won’t appear!

For our TODO App, we used a Neon database to store our to-do list online. A **database** stores organized information that an application can retrieve and update. When we sign in to the same account from another browser or computer, the app will retrieve our saved tasks from the database by using our account's `userId` to find the tasks that belong to us!

Databases have:

* **Table**: groups related information together.
* **Row**: is one record in a table. In our task table, a row would be one task.
* **Column**: stores one kind of information about each record, such as, title, completion status, difficulty.

Table example:

| id | title | completed |
| :--- | :--- | :--- |
| 001 | Finish essay | false |

## Navigating Neon

In Lesson 1, you should’ve opened the Neon Console to see the project that is connected to your Codex app.

You can view your existing table by:

1. Click on your project  
2. Open up the **Postgres database** category in the left sidebar  
3. Open `Tables`

To see how the database works, you can test the following:

1. Create a task called `Find this task`  
2. Refresh the Neon table view and find its row.  
3. Update the title through your app.  
4. Refresh the table view again to see the change.
5. Delete the task through your app and confirm the row disappears.

## Let’s think about it

* [ ] Submit a screenshot of your database tables in Neon.
