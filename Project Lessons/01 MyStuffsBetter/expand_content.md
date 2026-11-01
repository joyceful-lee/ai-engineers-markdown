# Expand It

Jamie tested the site with his friend, Devin.

```talker
{
name: Jamie
bubble: speech
face: 🧑
}
I uploaded my collection to MyStuffBetter and sent it to Devin. He hated how good my binder looked!
```

Awesome! So we hit the goal.

```talker
{
name: Devin
bubble: speech
face: 😎
}
I tried to make my own, but the website made me make an account before I could even add a card. I didn't really want to share anything, I just wanted to try it out a bit. I don't like signing up for accounts unless I really have to.
```

That's a change we can make.

## Guest Mode and Browser Storage

We're going to add a **guest mode** that lets someone use part of our site without signing in. For MyStuffsBetter, guests can create and organize binders while their collection stays in that browser.

We'll use **localStorage** to keep guest binders and card data after a page refresh. After they get used to using the site, they can choose to create an account and port their data in `localStorage` to the Neon database!

This idea has a name: **Progressive Sign Up**. It's the idea that a website should try and be as open as possible without an account, and only ask you to sign up when it's actually necessary.

## Example

Devin chooses **Try as a guest**, creates a binder, and adds three cards. After refreshing the page, the binder and cards are still there. A message explains that the collection is saved only in this browser.

When Devin creates an account, their binder, cards, pictures, and chosen order move into their account without having to enter them again. From that point on, changes are saved to Neon, and uploaded images are stored in Vercel Blob.

## New Goal

Let visitors try collecting as guests, then move their collection into an account when they sign up or log in.

```checklist
{
title: Updated Project Requirements
color: #e7f7dc
}
- Add a clear option to continue as a guest.
- Let guests create, edit, delete, and organize their own binders and cards.
- Save guest binder and card data in localStorage so it survives a page refresh.
- Support optional card pictures within browser storage limits, and explain when a picture or collection cannot be saved.
- Tell guests that their collection stays in this browser and may be lost if browser data is cleared.
- Require an account to publish or share binders, like collections, and subscribe to updates.
- When a guest signs up or logs in, upload their binders and cards to Neon and their images to Vercel Blob.
- Keep any binders already in the account and avoid creating duplicates if an interrupted upload is retried.
- Remove the guest browser copy only after the entire collection has been saved successfully. If saving fails, keep the browser copy and provide a way to retry.
- After the move, save account collection changes to Neon rather than localStorage.
- Keep the guest and signed-in layouts, labels, and controls consistent.
```

## Let's think about it

How does guest mode work on your site, and when do you invite guests to sign up?
