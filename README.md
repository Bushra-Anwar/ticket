# Royal Cinema · Vercel static deployment

## Files

- `index.html` — customer cinema site
- `city_lite_cinema_erp_multi_counter_role_login.html` — Super Admin / Branch Manager workspace
- `city_lite_f_b_counter_pos_role_login.html` — F&B Counter POS
- `city_lite_cinema_erp_command_center_role_login.html` — Ticketing / Entry workspace
- `vercel.json` — route aliases (`/super-admin`, `/pos`, `/ticketing`)

## Deploy

Upload this folder to a Git repository and import that repository in Vercel. Choose **Other** as the framework preset, leave the build command empty, and use `.` as the output directory. The project is static HTML; `index.html` is the home page.

## Backend note

The pages call `/api/auth/register`, `/api/auth/login`, and `/api/bookings/confirm` when hosted. Those backend API services and a persistent database/payment gateway are not part of this static bundle; configure the existing cinema backend at the same domain before using live account or booking/payment flows. The HTML pages and their embedded CSS/JavaScript are included.
