# Expand It

Tammy was thrilled the first version of **Bobathon** actually worked! After a busy week, she wanted to understand how people are using the site.

```talker
{
name: Tammy
bubble: speech
face: 🧋
}
The builder makes ordering easier, but I still have to look through individual orders to see which toppings are popular. I'd like to know what customers choose most often.
```

To help Tammy, we'll add a private dashboard that helps staff understand their customers better.

## Admin Analytics

**Admin analytics** turn saved activity like usage, engagement, and patterns into useful insights for the people running a site. For Bobathon, reports might show popular toppings, common drink combinations, or the average value of a completed order. Tammy can use this information to plan ingredients or improve the menu.

The dashboard should explain what each number represents and which dates it covers. Because staff reports contain information about the shop's activity, they need authentication and server-side staff permission checks.

## Example

Tammy signs in and selects the past seven days. The dashboard shows that tapioca pearls were the most popular topping and that the average completed order cost $6.

## New Goal

Give authorized staff a dashboard that explains what customers order most often, while keeping the customer builder working as before.

```checklist
{
title: Updated Project Requirements
color: #e7f7dc
}
- Add a private staff dashboard using actual Neon data from saved orders and builder activity.
- Show popular ingredients, common drink combinations, and average completed-order value, with clear metric definitions and reporting date filters.
- Let staff select a reporting date range and explain what each metric measures.
- Protect staff access with Neon authentication.
```

## Let's think about it

Which question can Tammy answer using your dashboard, and what saved information is needed to calculate that answer?
