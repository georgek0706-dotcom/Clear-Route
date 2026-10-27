ClearRoute MVP (2026-10-27)
================================
This is a mobile-first Progressive Web App using Mapbox GL JS, Geocoding v6, and Directions v5 driving-traffic.

TO TEST ON IPHONE
1. Host these four files together on an HTTPS static site (for example GitHub Pages, Cloudflare Pages, Netlify).
2. Open the URL in iPhone Safari. Allow location access.
3. Search and select a destination from the autocomplete list.
4. Find routes, choose Fastest/Balanced/Avoid traffic, then Start driving.
5. Safari > Share > Add to Home Screen.

WHAT IT DOES
- Uses iPhone GPS (HTTPS required).
- Searches destinations and fetches up to 3 routing alternatives from Mapbox.
- Scores alternatives using traffic-aware duration and congestion_numeric when available.
- Rechecks route options every 30 seconds while active/visible.
- Displays time, arrival time, mileage, and congestion score.

IMPORTANT LIMITATIONS
- Cannot generate arbitrary uncongested side-street alternatives that Mapbox does not return.
- Score is based on traffic coverage; unknown segments cannot be assumed clear.
- Route reassessment is NOT full spoken turn-by-turn navigation, nor dependable background tracking.
- During reroute updates the visual route changes, but no road-following maneuver instructions are given.
- Avoid Traffic remains bounded to returned alternate routes; it may share the same route as Fastest.
- On mobile Safari the page needs to be in foreground with display awake.
- This is a prototype for testing parked or with a passenger, not a replacement for navigation while driving.
- Your Mapbox token is a public pk token in client-side code; consider setting allowed URLs and quotas in Mapbox dashboard before public hosting.
- Traffic/maps/routing/search can incur API costs beyond Mapbox free allowances.
