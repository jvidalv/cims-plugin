---
name: find-vertical-routes
description: Find via ferratas, canyoning descents and rock climbing crags, and explain their grade, gear, timing and access. Use when someone asks about a ferrata, a barranc or canyon, or a crag or sector to climb, by place, grade, season or discipline.
---

# Find ferratas, canyons and crags with Cims

Use the Cims connector's tools, in the user's language. Searches near a place take its coordinates and return the nearest first.

## Via ferratas

`search_ferratas` filters by `grade` band (easy is K1, moderate K2–K3, hard K4, extreme K5–K6), `feature` (zip-line, bridge), `country`, `region` and `openOnly`. `get_ferrata` gives the K grade, cable length, drop, approach, route and descent times, status and ratings.

## Canyons

`search_canyons` filters by `grade` band and `water` (dry or aquatic). `get_canyon` gives the vertical and aquatic grades, commitment, number and length of rappels, the rope and wetsuit needed, timings, escape points and restrictions.

## Crags

`search_crags` filters by `grade` band, `approachMax` in minutes and `accessOpen`. Its `discipline` and `season` filters only match crags that record them, and most don't yet, so search without them and judge style and season from `get_crag`, which lists the sectors with their aspect, approach and first routes, the rock and any access restriction.

## Answer

- Lead with the best match and say why it fits: grade, time, season, distance.
- Give the gear and the timings the result lists, and any closure, permit or seasonal restriction in full. Never leave out a restriction to make an option look better.
- Link each result's `url` on fescims.com.

These are serious activities. Say plainly when an option is beyond what the user described, and that grades, conditions and water levels change: they should check recent reports and go with someone experienced if they are new to it.
