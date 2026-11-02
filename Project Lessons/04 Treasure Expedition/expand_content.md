# Expand It

Noah has unlocked several locations, but lost interest in continuing to travel through the map.

```talker
{
name: Noah
bubble: speech
face: 🗺️
}
Getting an answer right doesn’t feel satisfying when all that happens is moving on to the next question.
```

Great point. We can add a feature where players can work to complete a collection and exchange rewards with one another.

## Completionism and Trading

**Completionism** is the motivation to discover every item, explore every location, or finish every goal.

For our site, completing each checkpoint will earn Noah a collectible reward. A varied collection with different rarities will give him something to look forward to as he learns and explores.

**Trading** lets players exchange items they own. Someone with a duplicate may have exactly what another player is missing, so trading gives players another way to work toward their collection goals.

A trade must check who owns each item and update both inventories together. That prevents an interrupted or repeated request from duplicating items or leaving one player without their reward.

## Example

Noah’s collection page shows eight of twelve treasures found and a clue about where another might be discovered. Noah offers a duplicate compass for another player's extra crystal. If another player accepts, both inventories update, and Noah’s collection now shows nine discoveries. The same trade cannot be accepted again.

## New Goal

Give players clear collection goals and a safe way to trade while preserving learning progress.

```checklist
{
title: Updated Project Requirements
color: #e7f7dc
}
- Award a random collectible reward after each completed checkpoint, with different levels of rarity.
- Visualize the collection by rarity, showing owned rewards, duplicates, and missing items.
- Add a trading post where players offer owned rewards and request others
- Let players accept available trades or cancel their own pending offers.
- Validate ownership and exchange items together, preventing conflicting or duplicate trades.
```

## Let's think about it

How does your site show what remains to be discovered?
