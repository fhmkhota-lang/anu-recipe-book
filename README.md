# Anu's Recipe Book

A searchable digital edition of Anu's handwritten recipe notebooks — 188 photographed pages transcribed into **155 recipes** of South African Indian home cooking, from Steers Saucy Chicken and Mince Pilau to Malva Pudding and Hertzoggies. You can add your own recipes and photos to it too.

**[Open the recipe book →](https://fhmkhota-lang.github.io/anu-recipe-book/)**

## Features

- **Search** every recipe by name, ingredient or tag, and browse by category
- **A gluten-free version of every recipe** — flip one switch and the whole book shows gluten-free ingredients, with the original struck through so you can see what changed, plus the technique notes that actually matter (gluten-free dough gets one rise, not two) and a list of bought items whose labels need checking
- **Add your own recipes** — they join the search, planner and fridge matcher alongside the notebook ones, and can be edited or deleted later
- **Start from a link** — paste a recipe page, blog post or video and the book pulls out the ingredients and method for you to check before saving
- **Photos** on any recipe, yours or Anu's — snap the finished dish, add as many as you like, tap to enlarge
- **Week planner** — assign dishes to days, or let the book fill the week for you
- **What's in the fridge** — list what you have and recipes are ranked by how close you are to making them
- **Shopping list** built automatically from the week plan, with tick-offs
- **Backup & restore** — save everything you've added to a file, move it to another device, or share it with family
- **Favourites**, a "surprise me" button, and tickable ingredients while you cook

Everything runs in a single `index.html` — no build, no server, no dependencies.

## Gluten free

Every recipe has a gluten-free version, worked out from its ingredient list rather than written out twice:

| | |
| --- | --- |
| 69 recipes | already gluten free as written |
| 30 recipes | need simple swaps (gluten-free pasta, tamari for soy sauce) |
| 56 recipes | need swaps **and** a change in method — mostly the baking |

The same rules run over recipes you add or import, so those get a gluten-free version too. Bought items that vary by brand — masalas, stock cubes, bottled sauces, baking powder — are flagged for a label check rather than silently swapped. **If you are cooking for coeliac disease, read the labels yourself; this is a cook's guide, not a medical one.**

## Importing from a link

Paste a URL on the *Add a Recipe* tab. Most recipe sites publish their recipe in a machine-readable form and those import cleanly, title, ingredients, method and all. Sites that block automated readers (AllRecipes, for one) and social posts that hide their text behind a login will not work — the book says so plainly and opens a box for you to paste the text instead, which always works. Pages are fetched through the public `r.jina.ai` reader, since a browser cannot read another site directly; only paste links you are happy to send through it. Nothing is ever saved automatically — the form is filled in for you to check.

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
