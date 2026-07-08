# Tasks: Browse the duck catalog

1. Create the local duck catalog data source
   - Add a seeded catalog with at least 10 ducks across at least 3 categories.
   - Acceptance check: a data-loading function returns the expected catalog entries and seed counts.
   - Dependencies: none

2. Implement the catalog rendering view
   - Render the home page catalog using the local data source.
   - Show each duck’s name, category, price, and tagline.
   - Acceptance check: the catalog view displays all required fields for each rendered duck.
   - Dependencies: Task 1

3. Add empty-state handling
   - Show a clear empty-state message when the catalog contains no ducks.
   - Acceptance check: when no entries are present, the page displays the empty-state message instead of a blank view.
   - Dependencies: Task 2

4. Add tests for the catalog behavior
   - Cover populated catalog rendering, empty-state rendering, and required field display.
   - Acceptance check: `vitest` passes for the catalog-related tests.
   - Dependencies: Tasks 2 and 3
