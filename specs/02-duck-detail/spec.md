# Spec: View a duck's detail page

## Problem
Customers need a way to inspect a single duck in detail before making a purchase. The application should present the full record for a selected duck and handle invalid IDs cleanly.

## Users
- Quincy Quacker (customer): wants to read a duck's full description, personality traits, price, and availability before buying.

## Scope (in/out)
### In scope
- Display a duck detail page for a valid duck ID.
- Render the duck name, category, price, tagline, long description, personality traits, and stock level.
- Show a clear "duck not found" response for invalid or unknown IDs.
- Ensure the catalog list links or refers to detail pages by duck ID.

### Out of scope
- Customer reviews.
- Related ducks recommendations.
- Checkout, cart, or purchasing flows.

## Functional requirements
1. Given a valid duck ID, the detail page must return the full duck record.
2. The full duck record must include: name, category, price, tagline, long description, personality traits, and stock level messaging.
3. Stock level must be displayed as a user-friendly message such as "In stock", "Only 2 left", or "Sold out".
4. An invalid or unknown duck ID must result in a clear "duck not found" response.
5. The catalog listing must include links or references that use the duck ID to navigate to the detail page.

## Non-functional requirements
- The duck detail page should render consistently in a standard browser environment.
- The implementation should remain simple and easy to extend for future stories.
- Error handling should be user-friendly and not expose internal application errors.

## Acceptance criteria
- A valid duck ID loads a detail page with name, category, price, tagline, long description, personality traits, and stock level.
- Invalid or unknown IDs show a clear "duck not found" response.
- The catalog list includes links or references to the detail page by duck ID.
- The detail page experience is consistent and usable regardless of duck availability.
