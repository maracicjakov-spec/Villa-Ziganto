# Villa Žiganto — website

A static, single-page site (EN / DE / HR / IT) for **Villa Ziganto with a view of the Kvarner Bay**, Poljane 62, 51414 Opatija, Croatia.
Primary source: the Booking.com listing — https://www.booking.com/hotel/hr/villa-ziganto-with-saltwater-pool.hr.html (read 15 Oct 2026).

## Structure

```
index.html        page, inline CSS + JS (EN in the markup; DE / HR / IT in the `DE`, `HR`, `IT` objects — 182 keys each)
images/           54 photos as WebP at 640 / 1280 / 1920 px (hero also 2560 + portrait crop p828/p1242) + og-image.jpg
fonts/            Fraunces + Hanken Grotesk, self-hosted woff2 (latin + latin-ext)
favicon.svg
vercel.json       long-cache headers for /images and /fonts
```

No build step. Deploy the folder to Vercel as a static site. Local preview: `npx http-server -p 5188`.

## Before going live

1. **Inquiry e-mail:** set `CONFIG.inquiryEmail` at the top of the script. While it is empty, the form validates normally but shows an honest "demo mode — nothing was sent" message with a Booking.com link. Once set, inquiries go through FormSubmit (`formsubmit.co/ajax/<email>`) with Croatian labels for the host. The first submission triggers a FormSubmit activation e-mail that must be confirmed.
2. **Domain:** canonical, og:url, og:image and JSON-LD use the placeholder `https://villa-ziganto.vercel.app/`. og:image must stay an absolute URL.
3. **Photos:** all photos come from the Booking.com gallery (72 photos, downloaded at 2500 px). Get the owner's / agency's permission.
4. **Rating:** 10/10 from 2 reviews is an October 2026 snapshot and is labelled as such.

## Languages

EN default. Order: `?lang=` → saved choice (localStorage `vz-lang`) → browser language. Each language links to its own Booking.com page (`.en-gb`, `.de`, `.hr`, `.it`). The desktop nav appears from 1280 px (below that: burger menu + bottom bar), so the longer DE/IT labels fit on one line.

## Verified facts (Booking.com listing)

- Entire villa, 250 m². 4 bedrooms: bedrooms 1–3 each with 1 extra-large double bed, bedroom 4 with 2 single beds; sofa bed in the living room. 4 bathrooms; host text says each bedroom has an en-suite bathroom with shower.
- Private outdoor pool (seasonal), indoor jacuzzi/hot tub, garden, terrace, balcony, outdoor patio with sink and gas grill (summer kitchen), billiards
- Fully equipped kitchen, fridge, dishwasher, coffee machine, flat-screen TV, A/C, free Wi-Fi, free private parking, towels and bed linen
- Views: sea, pool, garden, courtyard
- Check-in 16:00–22:00 (tell the host your arrival time), check-out 07:00–10:00. €500 cash damage deposit, refunded after inspection. Minimum check-in age 26. Children of all ages, free cot 0–2 on request, no extra beds. No smoking, no parties, no pets.
- Distances (host text): Opatija 7 km, Ičići beach 4 km, first grocery store 150 m, Bistro Bussola / Restaurant Lučica / Restaurant Galeb 4 km. Lovran old town 6.9 km (Booking). Booking's OSM line for Ičići beach says 2.1 km (straight line); the site uses the host's 4 km.
- Coordinates 45.3188963, 14.2708245
- Score 10 "Exceptional" from 2 reviews; categories 10 except location 8.8. Booking.com quality rating 4/5.
- Managed by Davorowski Holiday Homes (9.6 average, 1,383 reviews, 186 properties). Staff speak German, English, Croatian.
- Spelling: Booking writes "Ziganto"; the facade sign and the host text say **"Villa Žiganto"** — the site uses Žiganto.

## Unverified — not claimed on the site, confirm with the owner

- **Maximum guests.** Booking says max 4 adults, but there are beds for 8 + a sofa bed. The site gives no guest count (the inquiry form allows up to 8 adults — adjust when confirmed).
- **Saltwater pool.** Only the Booking URL slug says "with-saltwater-pool"; not mentioned on the site.
- Pool size, heating, season dates.
- Washing machine/dryer are visible in the games-room photo but not listed by Booking — not mentioned.
- Tennis court and fishing appear in Booking's generic "activities" list — not mentioned.
- Prices: the 2027 June week showed €5,243 for 4 adults; the site shows no prices.
- Direct phone / e-mail: not public on Booking.

## Photo map (Booking order → file)

04 `dusk-aerial` (hero, day-story 21:00) · 25 `exterior-pool` (intro) · 50 `balcony-view` · 21 `living-gold` · 20 `living-view` · 15 `hall-stairs` · 23 `dining-art` · 14 `kitchen` · 24 `coffee-corner` · 00 `jacuzzi-view` · 48 `jacuzzi-room` · 70 `billiard` · 09/11/12/10 bedrooms · 30/28/26 baths · 02 `pool-sea` · 62 `pergola-dining` · 03 `pool-umbrella` · 55 `terrace-dining` · 07 `summer-kitchen` · 67 `garden-olive` · 68 `aerial-top` · 54 `balcony-pool` · 60 `location-aerial` (photo already has a pin on the villa) · plus gallery-only images.
Not used: 13 (WC detail), 27/29 (near-duplicate baths), 31/32/34/35/37/39/41–43/47 (near-duplicate rooms/corridors), 57/58 (street view), 65, 69 (plot outline drawing).
