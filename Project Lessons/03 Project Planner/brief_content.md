## Meet Your Client

**Quinn is in charge of fundraising for her school club and leading a group project for science class.** She's been having trouble managing all her responsibilities and deadlines. **What do we do?**

```talker
{
name: Quinn
bubble: speech
face: 🗂️
}
I asked three people for the status of the same task and got three different answers. Then I found out the task was finished two days ago!
```

Since projects include groups, roles, tasks, and deadlines, Quinn needs an organized way to manage everything. Each team member should have access to the information they need based on their role.

```talker
{
name: Quinn
bubble: speech
face: 🗂️
}
I want to be able to assign my team members tasks and have them be able to update their own work.
```

Giving users different levels of access based on their responsibilities is called **user permissions**. For example, a manager can assign work and edit deadlines, a member can update their assigned tasks, and a viewer can read progress.

Hiding a button is not enough. The server must check the user's group, project, and role before allowing a change.

## Your Goal

Build **Project Planner**, where users can lead projects, invite members, assign tasks, update deadlines, and track progress together.

Use GitHub to upload your code, Neon for authentication and database storage, and Vercel for deployment.

```checkbox
{
title: Project Requirements
color: #e7f7dc
}
- Let users sign up, log in, and log out.
- Let a user create projects, invite accounts, and manage member roles.
- Create tasks with titles, descriptions, assignees, due dates, priorities, and statuses; require lead approval for member submissions.
- Add a visual element to organize deadlines and due dates in an easy-to-read manner
- Be able to lead or be a member of multiple projects
- Keep group and project information accessible only to the appropriate members.
```

## Let's think about it

- [ ] I've read the project brief and I'm ready to plan.
