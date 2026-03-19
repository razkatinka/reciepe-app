[README.md](https://github.com/user-attachments/files/26123660/README.md)
# מוצא מתכונים — Recipe Finder

A Hebrew-language, single-file recipe finder app. No backend, no API, no dependencies — just open `index.html` in a browser.

## What It Does

Enter ingredients you have at home and the app finds matching recipes from a built-in database of 20 recipes. Recipes are ranked by how many of your ingredients they use. The app covers a variety of cuisines and dietary preferences: breakfast, lunch, dinner, vegetarian, vegan, meat dishes, Mediterranean, Middle Eastern, Asian, and Italian.

## How to Use

1. **Add ingredients** — type an ingredient and press Enter or comma to add it as a chip. Remove chips with ×.
2. **Filter** — select a meal type (breakfast / lunch / dinner) and/or dietary preference (vegetarian / vegan / meat).
3. **Search** — click "חפש מתכונים". Recipes that match 50% or more of their ingredients appear, sorted by match percentage.
4. **Open a recipe** — click any card to expand it and see the full recipe.
5. **Adjust servings** — use the +/− buttons to rescale all ingredient amounts for the number of people you're cooking for.
6. **Cook with the steps** — tap each step to mark it as done. Steps with a time estimate have a built-in countdown timer; tap the timer button to start it. An audio alert plays when it finishes.
7. **Shopping list** — ingredients you don't have show an "add to list" button. View, check off, or clear the list via the 🛒 button. The list is saved across sessions.
8. **Favorites** — tap the heart on any card to save it. Favorites persist in localStorage.
9. **Surprise me** — click "הפתע אותי" to open a random recipe (respects active filters).

## Tech Stack

| Layer | Details |
|---|---|
| Markup | HTML5, `dir="rtl"` for right-to-left Hebrew layout |
| Styling | Vanilla CSS with custom properties, CSS Grid, responsive layout |
| Fonts | [Heebo](https://fonts.google.com/specimen/Heebo) via Google Fonts |
| Logic | Vanilla JavaScript (ES6+), no frameworks |
| Audio | Web Audio API for timer alerts |
| Persistence | `localStorage` for favorites and shopping list |
| Data | 20 recipes as a static JS array — no external data source |

## Running Locally

No build step or server required.

```bash
# Clone or download the repo, then just open the file:
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

Or drag `index.html` into any modern browser (Chrome, Firefox, Edge, Safari).

> **Note:** The Google Fonts stylesheet loads from the internet. The app works offline without it — it falls back to the system sans-serif font.
