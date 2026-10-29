---
name: explore-peak-challenges
description: Explain the peak-bagging challenges in Cims, such as the 100 Cims of Catalonia, which peaks they include, which are essential, and who leads them. Use when someone asks about a list of peaks to climb, the 100 Cims, the essentials, a challenge in a region, or the community ranking.
---

# Explore peak challenges with Cims

Use the Cims connector's tools, in the user's language.

## Find the challenge

Call `list_challenges`. Each challenge has a `slug`, how many peaks it has, how many are essential (must-climb), how many people take part and where its peaks are. Match the user's words to the right one; if two fit, ask which.

## Browse its peaks

Call `peaks_nearby` with `challengeSlug`. Add a point (`lat`, `lng`) to start from where the user lives, `essentialOnly` for the must-climb peaks, `sort: "height"` for the highest, and `altitudeBands` to narrow by height. Results come in pages of up to 50; ask the user to narrow down rather than paging through the whole list.

## Ranking

Call `challenge_leaderboard` with the `challengeSlug` for the public ranking: validated summits, distinct peaks, essentials and score. The score weighs height climbed and counts essentials extra.

## Answer

Describe the challenge in a sentence or two, then answer what was asked: a few peaks to start with near the user, the essentials, or the ranking. Link each peak's `url` on fescims.com.

The connector reads only the public catalogue. It cannot see the user's own summits or progress, so if they ask what they have left, say that their progress is in the Cims app.
