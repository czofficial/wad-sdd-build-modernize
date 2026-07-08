# Plan: Browse the duck catalog

## Data model
- Introduce a `Duck` model with fields for:
  - `id`
  - `name`
  - `category`
  - `price`
  - `tagline`
- Store catalog data in a local JSON source so the app can read it without a backend.
- Keep the data shape simple and reusable for later stories such as detail pages and cart integration.

## Module / file layout
- Add a small catalog data module for loading and seeding ducks.
- Add a view or component responsible for rendering the home page catalog.
- Keep the presentation layer separate from the data access layer so future changes remain localized.
- Suggested structure:
  - `src/data/ducks.ts` or similar for catalog data access
  - `src/components/CatalogView.tsx` (or equivalent) for rendering
  - `src/pages/HomePage` or similar entry point for composing the view

## Public interfaces
- Expose a function such as `getDucks()` that returns the available catalog entries.
- Expose a helper for loading seeded data from local storage or a local JSON file.
- Ensure the UI consumes a single, consistent catalog data interface.

## External dependencies
- Prefer no new external libraries for this story.
- Use the existing app runtime and local storage or file-based data access already supported by the project.
- If the project already has a testing setup, use that existing test runner rather than introducing new tooling.

## Testing strategy
- Add unit or component tests for:
  - rendering a populated catalog
  - rendering the empty-state message when no ducks are available
  - correct display of required fields for each duck card
- Verify that the seeded local data includes at least 10 ducks across at least 3 categories.

## Risks
- The catalog data source may be implemented inconsistently if the app has no existing pattern for local data.
- Empty-state handling could be overlooked if the UI assumes the catalog is always populated.
- The seed data must remain realistic and sufficiently varied to support future stories.
