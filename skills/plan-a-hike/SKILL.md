---
name: plan-a-hike
description: Suggest a peak to climb and a trail to climb it by. Use when someone asks for a hike, a summit or a day out in the mountains, mentions a town, comarca, valley or peak in Catalonia, the Pyrenees or Spain, or wants something easy, family- or dog-friendly, short, long or with a view.
---

# Plan a hike with Cims

Use the Cims connector's tools, in the user's language.

## 1. Find where

- **A peak by name:** call `search_peaks` with the name and keep the `slug`.
- **A town, village or valley** ("near Berga", "from Núria"): use its approximate `lat` and `lng` as the point for the next calls. Searching a town name with `search_peaks` can match a different place entirely ("Berga" finds Bergamo).
- **A comarca, province or country** ("in the Berguedà"): call `search_peaks` with it as `query` and use the `lat` and `lng` of the results as the point.
- **Coordinates the user gave you:** use them directly.

## 2. Pick the peak

Call `peaks_nearby` with the point and a `radiusKm` that fits the trip (10–20 km for a day out). Narrow with what the user asked for:

- `familyFriendly` or `dogFriendly` for families and dogs.
- `altitudeBands` for a height range.
- `essentialOnly` for the peaks a challenge marks as must-climb.
- `sort: "recommended"` when the user only wants a good idea.

Then call `get_peak` on the one or two strongest candidates. Use its community ratings (1–5, with the number of votes), its recent summits and its comments to judge how it is going this season.

## 3. Pick the trail

Call `search_trails` with `peakSlug`, or with the point when the user cares about the trailhead. Match the request with `difficulty`, `distanceBands`, `ascentBands`, `shape` (loop, out-and-back, one-way), `suitableFor`, `easyParking` and `scenery`. `suitableFor`, `scenery` and `easyParking` come from community votes, so many good trails have none: if one of them empties the list, search again without it and judge from distance, ascent and difficulty. Call `get_trail` on the best one for times, ascent, the start point and the Wikiloc link.

## 4. Answer

Give one clear suggestion first, then one or two alternatives. For each:

- the peak, its height and the trail's distance, ascent, estimated time and difficulty;
- why it fits what the user asked;
- the peak's `url` on fescims.com and the trail's Wikiloc link.

Ratings with few votes are a hint, not a verdict, so say how many votes there are. Remind the user to check the weather and conditions before going: the catalogue does not know today's snow, storms or closures.

If nothing fits, widen the radius or relax one filter and say which one you relaxed.
