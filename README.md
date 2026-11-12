# Dishly – Meal Search App (Vue 3)

A responsive web app to find recipes, using the free [TheMealDB API](https://www.themealdb.com/api.php).

## Features

- **Search by name** with live results.
- **Browse by first letter** (A–Z).
- **Browse by ingredient**: list of ingredients, then the meals that use one.
- **Meal details**: picture, ingredients with measures, instructions, and links to the YouTube video and original source.
- Responsive layout with Tailwind CSS.

## Tech stack

Vue 3 · Vite · Vue Router · Vuex · Axios · Tailwind CSS

## Routes

| Path | Page |
|---|---|
| `/` | home |
| `/by-name/:name?` | search by name |
| `/by-letter/:letter?` | browse by letter |
| `/ingredients` | all ingredients |
| `/by-ingredient/:ingredient` | meals with one ingredient |
| `/meal/:id` | meal details |

## Run it locally

```bash
npm install
npm run dev
```

The API base URL is set in `.env` as `VITE_API_BASE_URL` (TheMealDB public endpoint, no key needed).

## Author

Ridha Lezzar · [LinkedIn](https://linkedin.com/in/ridha-lezzar-8322222b5)
