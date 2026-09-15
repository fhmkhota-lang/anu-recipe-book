# Anu's Recipe Book

A searchable digital edition of Anu's handwritten recipe notebooks — 188 photographed pages transcribed into **155 recipes** of South African Indian home cooking, from Steers Saucy Chicken and Mince Pilau to Malva Pudding and Hertzoggies. You can add your own recipes and photos to it too.

**[Open the recipe book →](https://fhmkhota-lang.github.io/anu-recipe-book/)**

## Features

- **Search** every recipe by name, ingredient or tag, and browse by category
- **Add your own recipes** — they join the search, planner and fridge matcher alongside the notebook ones, and can be edited or deleted later
- **Photos** on any recipe, yours or Anu's — snap the finished dish, add as many as you like, tap to enlarge
- **Week planner** — assign dishes to days, or let the book fill the week for you
- **What's in the fridge** — list what you have and recipes are ranked by how close you are to making them
- **Shopping list** built automatically from the week plan, with tick-offs
- **Backup & restore** — save everything you've added to a file, move it to another device, or share it with family
- **Favourites**, a "surprise me" button, and tickable ingredients while you cook

Everything runs in a single `index.html` — no build, no server, no dependencies.

## Where your data lives

Nothing is uploaded anywhere. The book works entirely in your browser:

| What | Stored in |
| --- | --- |
| Favourites, week plan, fridge list, shopping ticks | `localStorage` |
| Recipes you add | `localStorage` |
| Photo thumbnails | `localStorage` |
| Full-size photos | `IndexedDB` (much roomier than localStorage's ~5 MB) |

Because it is per-browser, **use *Download backup* on the Add a Recipe tab** to keep a copy or move your recipes to your phone. Photos are resized on the way in (max 1400 px, ~60–120 KB each) so they don't fill up storage.

## Files

- [`index.html`](index.html) — the app, fully self-contained
- [`transcriptions.md`](transcriptions.md) — raw page-by-page transcriptions of the notebook, keyed to photo filenames

Family shorthand is kept as written: *dhana jeeru* (coriander-cumin), *arad* (turmeric), *vagaar* (tempering), *aamli* (tamarind), *gg* (ginger garlic).
