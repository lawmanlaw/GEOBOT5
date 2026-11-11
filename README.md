# GeoBots

Community crime mapping for Gaborone, Botswana.

A single-page web app: `index.html` has no build step and no dependencies to install. Open it in a browser, or host the folder on any static host.

## What it does

- Live crime map on OpenStreetMap, with three base styles
- Press and hold anywhere on the map to pin an incident on that exact spot
- Incident types, time, and an optional note
- Your location with a live accuracy circle
- Search Gaborone places, or anywhere in Botswana
- Insights: counts by type, share after dark
- Thusa! emergency flow with Police, Ambulance and Security
- GBV support: helplines, PIN-sealed private records kept on the device, and an option to show the section as "Notes"
- Trusted contacts and an alert radius
- Plans: Motse, Tsela, Sireletsa

## Not connected yet

These are built as screens and clearly say so in the app:

- Email sign in codes
- Payments (card, Orange Money, MyZaka, Smega, bank transfer)
- Thusa! does not dispatch anyone. It shows 999, 997 and 998
- Reports save to the browser on one device, not to a shared database

## Before launch

- Confirm the GBV helpline numbers with the Botswana Police Service and BGBVC
- Replace the example incidents with real data
- Move reports and accounts to a server, with access rules so a user can only reach their own data
- Keep every secret and key in server-side environment variables

## Hosting notes

Sealed GBV records use the Web Crypto API, which needs HTTPS. They will not save from a file opened directly off disk.

## Files

- `index.html` is the deployed site. It loads the map library and the font from a CDN and the photos as separate files, so it is small and fast on phone data.
- `standalone.html` is the same app with the library, font and photos built in. One file, works offline and off a USB stick, but much heavier.
