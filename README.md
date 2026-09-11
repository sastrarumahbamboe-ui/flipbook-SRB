# FLIPBOOK SRB — FULL

Full-stack starter for Jurnal Sastra Rumah Bamboe:
- Admin upload PDF
- Supabase Storage for online PDF
- PostgreSQL metadata
- Public reader URL per magazine
- iframe embed code
- responsive reader
- share/fullscreen/zoom/page navigation

## Setup
1. Create a Supabase project.
2. Run `supabase/schema.sql` in SQL Editor.
3. Create Storage bucket `magazines` and make it public for the simplest deployment.
4. Configure Storage INSERT/UPDATE/DELETE policies for authenticated admins before production.
5. Put your Supabase URL and ANON/PUBLISHABLE key into `public/admin/config.js`.
6. Upload `public/` to GitHub.
7. Enable GitHub Pages from the repository.
8. Open `/admin/` to publish a magazine.

## Security
Do NOT put a Supabase service-role/secret key in GitHub or browser code. For a production admin system, add Supabase Auth and authenticated Storage policies.

## Public URL
After publishing, the admin generates:
`/book/?id=DATABASE_ID`

## Embed
`<iframe src="PUBLIC_BOOK_URL" width="100%" height="700" style="border:0" allowfullscreen loading="lazy"></iframe>`

## Notes
This is a working starter architecture, not a clone of Heyzine's proprietary backend. The page-turn effect is intentionally implemented as a clean responsive reader; a more elaborate 3D page-turn engine can be added later.
