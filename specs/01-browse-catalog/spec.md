# Spec: Browse the duck catalog

## Problem
Visitors to The Rubber Duck Emporium need a simple way to see what ducks are currently available before deciding whether to purchase one. The home page should provide an immediate overview of the catalog so users can quickly understand the available options.

## Users
- Quincy Quacker (customer): wants to browse available ducks quickly and assess whether anything appeals to them.

## Scope (in/out)
### In scope
- Display a home page catalog of available ducks.
- Show each duck with at least name, category, price, and a one-line tagline.
- Load catalog data from a local data source.
- Seed the catalog with at least 10 ducks across at least 3 categories.
- Show an explicit empty-state message when no ducks are available.

### Out of scope
- Pagination.
- Images.
- Sorting controls.
- Advanced filtering or search.

## Functional requirements
1. The home page must render a list of ducks when the catalog contains data.
2. Each catalog item must display the duck name, category, price, and a short tagline.
3. The catalog data must be stored locally and available to the application without relying on a remote service.
4. The seeded catalog must contain at least 10 ducks spanning at least 3 categories.
5. If the catalog is empty, the user must see a clear empty-state message rather than a blank or broken page.
6. The page should remain usable even if the catalog has no entries.

## Non-functional requirements
- The experience should be lightweight and suitable for a workshop-level application.
- The catalog view should render reliably in a standard browser environment.
- The implementation should be easy to understand and extend for later stories.

## Acceptance criteria
- The home page returns a list of ducks.
- Each duck in the list shows at minimum: name, category, price, and a one-line tagline.
- The catalog is read from local storage (JSON file or SQLite). Seed it with at least 10 ducks across at least 3 categories.
- An empty catalog renders an explicit empty-state message — not a blank page.

## Open questions
- None at this stage; the story provides enough detail for implementation planning.
