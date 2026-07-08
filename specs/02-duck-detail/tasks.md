# Tasks: View a duck's detail page

**Input**: Design documents from [specs/02-duck-detail](specs/02-duck-detail)

**Prerequisites**: plan.md, spec.md, research.md, data-model.md, contracts/

## Phase 1: Setup (Shared Infrastructure)

- [x] T001 Create or confirm the feature implementation files in duck-emporium/src/
- [x] T002 [P] Ensure the existing Vitest setup can run the new detail-focused tests

## Phase 2: Foundational (Blocking Prerequisites)

- [x] T003 Extend the local duck data shape in duck-emporium/src/duck-catalog.ts to support the detail fields required by the story
- [x] T004 Add a reusable detail lookup helper in duck-emporium/src/duck-detail.ts for valid and invalid duck IDs

## Phase 3: User Story 1 - View a duck's detail page (Priority: P1) 🎯 MVP

**Goal**: Deliver a detail experience for a specific duck and a clear not-found state.

**Independent Test**: Verify that a known duck ID returns the full record and an unknown ID returns a friendly not-found result.

### Tests for User Story 1

- [x] T005 [P] [US1] Add a unit test for a valid duck ID in duck-emporium/src/duck-detail.test.ts
- [x] T006 [P] [US1] Add a unit test for an invalid duck ID in duck-emporium/src/duck-detail.test.ts

### Implementation for User Story 1

- [x] T007 [P] [US1] Update the duck catalog data to include long descriptions, personality traits, and stock messaging in duck-emporium/src/duck-catalog.ts
- [x] T008 [US1] Implement detail lookup and not-found handling in duck-emporium/src/duck-detail.ts
- [x] T009 [US1] Ensure the catalog entries expose duck ID-based navigation references in duck-emporium/src/duck-catalog.ts

## Phase 4: Polish & Cross-Cutting Concerns

- [x] T010 [P] Add or update documentation for the detail flow in specs/02-duck-detail/quickstart.md
- [x] T011 Run the relevant Vitest suite and confirm the new detail tests pass

## Dependencies & Execution Order

### Phase Dependencies

- Setup (Phase 1): No dependencies
- Foundational (Phase 2): Depends on Setup completion
- User Story 1 (Phase 3): Depends on Foundational completion
- Polish (Phase 4): Depends on User Story 1 completion

### User Story Dependencies

- User Story 1 (P1): No dependencies on other stories

### Parallel Opportunities

- T002 can run in parallel with T001
- T005 and T006 can run in parallel
- T007 and T009 can be worked on in parallel once the shared data shape is agreed

## Implementation Strategy

### MVP First

1. Complete Phase 1 and Phase 2
2. Implement User Story 1 and validate the happy path and not-found path
3. Stop after the MVP story is verified

### Incremental Delivery

1. Add the shared detail lookup helper
2. Extend the local data model for richer detail content
3. Verify the catalog links and not-found state
