# ChatterNakama

Static GitHub Pages planner for weekly chatter shifts. Open `index.html` — there is no build step.

The plan is one Firebase Realtime Database object at `plan.json`:

- `chatters`: `{ name, color }[]`
- `profiles`: profile names
- `slots`: `"d<offset>|<profile>|<hour>"` → chatter name
- `ts`: last write, in milliseconds

`offset` is days from Monday of the current week. The page saves by replacing that whole object.

Add `?offline=1` to use sample data in the browser without reading or writing Firebase.
