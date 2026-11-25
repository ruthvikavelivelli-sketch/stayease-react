# StayEase – React + Vite

## Run locally
```
npm install
npm run dev
```
## Build
```
npm run build
```
## Deploy on Vercel
1. Push this folder to GitHub.
2. Vercel → New Project → import repo (Framework: Vite, Build: `npm run build`, Output: `dist`).

## Modules
- **User**: Home, Signup, Login (localStorage `users`), plus hotels/booking/payment pages
- **Admin**: Admin Login (`admin@stayease.com` / `admin123`), protected Dashboard, hotels/bookings/users/reviews/analytics pages

## Structure
- `src/pages`, `src/components`, `src/utils/auth.js` – React code
- `public/pages`, `public/admin` – pages not yet converted (original HTML)
- Converted so far: Home, Login, Signup, Wishlist, Loyalty Points, Notifications, Admin Login, Admin Dashboard

## Popular Places to Hotel Route Feature

On the booking confirmation page, use **View Popular Places, Distance & Map** to open the map page. The map page reads the latest booking from `localStorage`, shows the booked hotel/city/area, and lets the user choose a popular landmark, airport, or railway station in the supported city. **View Distance & Directions in Google Maps** opens Google Maps with the selected origin, booked hotel destination, and chosen travel mode. Google Maps calculates road distance and ETA. The hotel map is embedded on the page.

Supported destination city lists currently include Hyderabad, Bangalore, Goa, Mumbai, and Delhi. If a city is not recognized, Hyderabad is used as a fallback list; update the `popular` object in `public/pages/hotel-map.html` to add more cities.
