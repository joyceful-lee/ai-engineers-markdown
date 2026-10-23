# Accounts, Sessions, and Permissions

Our feed can save posts, but currently uses a temporary author. In this lesson, we'll replace the temporary author with real accounts and decide what each user is allowed to do.

1. Authentication and Profiles  
2. Permissions & Ownership  
3. Show Who's Signed In

## 1. Authentication and Profiles

**Authentication** is how an app checks who you are through signup and logins. After signing in, the app uses a **session** to remember you. Without it, an app would have to ask who you are every time you open a new page. Sessions typically end when you sign out, but they can also expire after a certain amount of time too.

Some authentication services store profile information too; however, in our app, we'll keep a profile table for the information features need and connect each profile to the signed-in account using their `userId`.

- **Account:** information used to sign in (email, password, session; managed by Neon’s Better Auth)  
- **Profile:** information about you (display name, bio, avatar; managed by you through a table)

The app will connect the two using a unique **userId.** When someone signs in successfully for the first time, our backend checks whether a profile exists for their user ID. If it doesn't, the app will create one!

Returning users keep the same profile instead of getting a new row every time they sign in. When that user creates a post or comment, the app saves the same user ID in its `authorId` field. This connects the content to its author's profile.

### Let’s think about it

- [ ] I understand the difference between auth accounts and profiles

## 2. Permissions & Ownership

In step 1, we covered how authentication can sign you in; however, that doesn’t mean every signed in user should be able to edit everyone else’s posts!

This is where **permissions** come in. Permissions control who can do what with our data (e.g., viewing, creating, editing, deleting).

**Ownership** identifies who a piece of data belongs to. For example, when you create a post, the app saves your `userId` as its author. Permissions allow you to edit or delete posts with your id while preventing other users from changing it.

### Access levels in this app

| Role | Who | Typical access |
| :---- | :---- | :---- |
| Anyone | Guests and logging in users | Can read public content |
| Authenticated | Logged in | Can create posts and comments |
| Owner only | The author | Can edit or delete their own content |

```text  
Add NeonAuth (Better Auth) to this app. Build signup first. Stop and let me test it before continuing.

Requirements:
- Users can sign up with email and password  
- Users can sign in and sign out  
- New posts and comments use the real logged-in user instead of the hardcoded test user   
- Anyone can read public posts and comments
- Only signed-in users can create posts or comments
- Derive `authorId` from the verified signed-in identity
- Only the author can edit and delete their own posts/comments.
- Only the profile owner can edit their profile.

Enforce these rules in trusted backend code or database access
policies, not only by hiding buttons.

Confirm that rejected
requests leave the records unchanged.
```

### Let’s think about it

- [ ] Create a test account with at least one post and confirm it appears in Neon correctly.

## 3. Show Who's Signed In

The **UI** or **User Interface** should look different depending on whether a user is logged in or not.

A logged out user or guest should see the feed and a sign in or sign up link whereas a signed-in user should see their profile information, post and comment forms, and a sign-out button.

```text  
Update the UI for this application to reflect the auth state:

- Navbar: show the logged-in user's name and a "Sign Out" button when authenticated; show a "Sign In" link when not  
- Post form: visible only when logged in, hidden otherwise  
- Comment form: visible only when logged in, hidden otherwise  
- Show a short "Sign in to post" message where the form would be for logged-out visitors  
```

### Tips

- Test in an incognito window to simulate a logged-out visitor before signing in.  
- Sign out and confirm forms disappear and the navbar reverts to "Sign In".

### Let's think about it

- [ ] Open an incognito window — you should see the feed but no forms  
- [ ] Sign in — forms appear and the navbar shows your name  
- [ ] Sign out — forms disappear and the navbar reverts to "Sign In"
