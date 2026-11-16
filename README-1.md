# Second Helpings: Food Donation Connection Platform

Connects people with surplus food to nearby NGOs and organizations that can distribute it.

## The problem

Restaurants, bakeries, markets, event caterers and households often have good food they can’t use before it spoils. Shelters, community kitchens and food banks need it, but there is no quick way for the two sides to find each other in time.

## How it works

1. **A donor posts food.** They enter what it is, its type, the number of servings, the pickup area, and how long it stays safe to collect.
2. **The platform matches it.** Organizations that accept that food type are ranked by distance, and the closest ones are notified.
3. **An organization claims it.** Listings are shown soonest-to-expire first. One tap claims the pickup, and the listing is removed for everyone else.
4. **The donor sees the result.** Their listing shows its status, and a running tally tracks servings rescued.

## Current features (prototype)

- Donor form with food type, servings, pickup area and safe-to-collect window
- Nearest-organization matching based on accepted food types
- Organization view with a feed sorted by time left and distance
- Claim flow with listing status updates
- Live countdown on each listing, with urgent items highlighted
- Responsive layout, light and dark themes, keyboard-accessible controls

## Food types

Cooked meals, fresh produce, bread and bakery, packaged (sealed), dairy and chilled.

## Run it

The prototype is a single self-contained file, `food-donation-platform.html`, with no build step and no dependencies. Open it in any modern browser.

Sample organizations and listings are included for demonstration. State is kept in the browser’s local storage, so data is not shared between users or devices.

## Known limitations

- Distance uses a small set of named areas, not real coordinates
- No accounts, verification or notifications
- No shared backend, so a donor and an organization can’t yet use it on different devices

## Roadmap

1. Real location search and distance (address lookup, maps)
2. Accounts, with verification for organizations
3. Shared database so listings sync across users
4. Notifications by SMS, email or push when a matching listing is posted
5. Pickup coordination: time slots, driver or volunteer assignment
6. Food-safety guidance and handling checklists at posting time
7. Impact reporting: servings rescued, by donor and by organization
8. Multi-language support

## Suggested tech for a production version

- Frontend: React or plain web components, as a PWA so it works well on phones
- Backend: Node.js or Python API with PostgreSQL (PostGIS for location queries)
- Notifications: Twilio or a similar SMS and email provider
- Maps: OpenStreetMap-based geocoding to avoid vendor lock-in

## Food safety note

Donors are responsible for the safety of what they list. A production version should show local food-donation guidance and liability protections (for example, Good Samaritan laws where they apply) and require donors to confirm food was stored safely.

## License

To be decided.
