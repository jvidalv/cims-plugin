# Cims

Plan hikes, summits, multi-day traversals, via ferratas, canyons and climbing
crags with [Cims](https://fescims.com), the mountain community and catalogue
centred on Catalonia, the Pyrenees and Spain.

## What it does

The plugin connects Claude to the public Cims catalogue and teaches it four
workflows:

- **Plan a hike:** find a peak near a town, valley or point, then the trail to
  climb it, filtered by difficulty, length, ascent, families or dogs.
- **Plan a traversal:** choose a multi-day route such as Carros de Foc, read
  its stages and find the peaks to add along the way.
- **Find vertical routes:** via ferratas, canyoning descents and climbing
  crags, with grades, gear, timings, seasons and access restrictions.
- **Explore peak challenges:** the 100 Cims and other lists of peaks to climb,
  their essential peaks and the community ranking.

Answers link to the matching pages on fescims.com and to the original Wikiloc
tracks.

## Use it

In Claude Code, add this repository as a marketplace and install the plugin:

```
/plugin marketplace add jvidalv/cims-plugin
/plugin install fescims@fescims
```

In Claude chat or Cowork, install it from Claude's directory once it is listed
there, then connect the **Cims** connector from the plugin's Connectors tab.
It needs no account and no sign-in. Then ask, for example:

- "A family hike with a summit near Berga this Sunday"
- "Is Carros de Foc doable in four days, and which peaks can I add?"
- "An easy via ferrata near Montserrat"
- "Which are the essential peaks of the 100 Cims in the Pyrenees?"

## Data

The plugin talks to one server, `https://api.fescims.com/api/mcp`, which Cims
runs. Claude sends it the search terms, places, coordinates and filters of each
request, and it returns public catalogue data only. The plugin sends nothing
else, runs no code on your machine and needs no credentials. The server keeps
your IP address briefly to rate-limit requests. See the
[privacy policy](https://fescims.com/en/privacy-policy) and the
[connector guide](https://fescims.com/en/ai).

It cannot see your own summits or progress: those stay in the Cims app.

## Support

Write to us through [fescims.com/en/contact](https://fescims.com/en/contact).
