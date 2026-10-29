---
name: plan-a-traversal
description: Help choose and prepare a multi-day hut-to-hut or long-distance traversal, such as Carros de Foc, the Porta del Cel or a GR stage route. Use when someone asks about a trek of several days, refuges, stages, or which peaks they can add along the way.
---

# Plan a traversal with Cims

Use the Cims connector's tools, in the user's language.

## 1. Choose the traversal

- **By name:** call `search_traversals` with the name as `query`.
- **By area:** call `search_traversals` with the area's approximate `lat` and `lng`.
- **By ability and time:** filter with `effort`, `maxGrade` (the SAC hiking grade, T1 to T6 as 1 to 6) and `maxDays`.

## 2. Read it in full

Call `get_traversal` with the `slug`. It returns the totals, the SAC grade and its crux, whether it is circular, every stage with distance and ascent, the peaks along the way and photos.

## 3. Answer

- Summarise the route: days, total distance and ascent, grade and crux, start point, circular or not.
- List the stages in order, each with its start and end, distance and ascent. Point out the hardest one.
- Suggest summits to add: peaks marked `onTrack` lie on the route; the others are short detours from the stage they belong to. Use `get_peak` if the user wants detail on one of them.
- Link the traversal's `url` on fescims.com, and credit the photos and track source as the result gives them.

Refuges need booking and the high stages depend on snow and weather, so tell the user to confirm both before setting off.
