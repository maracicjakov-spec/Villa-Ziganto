# Villa Žiganto — website

A static, single-page site (EN / DE / HR / IT) for **Villa Ziganto with a view of the Kvarner Bay**, Poljane 62, 51414 Opatija, Croatia.
Primary source: the Booking.com listing — https://www.booking.com/hotel/hr/villa-ziganto-with-saltwater-pool.hr.html (read 15 Oct 2026).

## Structure

```
index.html        page, inline CSS + JS (EN in the markup; DE / HR / IT in the `DE`, `HR`, `IT` objects — 182 keys each)
images/           30 photos (MyLuxoria) as WebP at 640 / 1280 / 1920 px (hero also portrait crop p828/p1242) + og-image.jpg
fonts/            Fraunces + Hanken Grotesk, self-hosted woff2 (latin + latin-ext)
favicon.svg
vercel.json       long-cache headers for /images and /fonts
```

No build step. Deploy the folder to Vercel as a static site. Local preview: `npx http-server -p 5188`.

## Before going live

1. **Inquiries → WhatsApp:** the form (name, dates, adults, children, message) opens WhatsApp (`CONFIG.whatsapp` = wa.me/38598297179) with a prefilled Croatian message; the guest only taps Send. No e-mail service, nothing to activate. Phone, WhatsApp and e-mail (arnold.ziganto@gmail.com) are shown as plain contacts. No Booking.com links anywhere (owner wants direct bookings, no commission); the Booking rating is still quoted as text.
2. **Domain:** canonical, og:url, og:image and JSON-LD use the placeholder `https://villa-ziganto.vercel.app/`. og:image must stay an absolute URL.
3. **Photos:** since 3 Nov 2026 all photos come from MyLuxoria (https://www.myluxoria.com/hr/vile-opatija/villa-ziganto, 31 photos, one duplicate dropped) at the owner's request — the old Booking.com/Davorowski photos were removed. MyLuxoria originals are only 1600 px wide, so there is no 2560 hero. There is no dusk or drone photo, so the hero is a daytime shot and the 21:00 "villa lights up" step became 19:30 "Dinner by the grill".
4. **Rating:** 10/10 from 2 reviews is an October 2026 snapshot and is labelled as such.

## Languages

EN default. Order: `?lang=` → saved choice (localStorage `vz-lang`) → browser language.en-gb`, `.de`, `.hr`, `.it`). The desktop nav appears from 1280 px (below that: burger menu + bottom bar), so the longer DE/IT labels fit on one line.

## Verified facts (Booking.com listing)

- Entire villa, 250 m². 4 bedrooms: bedrooms 1–3 each with 1 extra-large double bed, bedroom 4 with 2 single beds; sofa bed in the living room. 4 bathrooms; host text says each bedroom has an en-suite bathroom with shower.
- Private outdoor pool (seasonal), indoor jacuzzi/hot tub, garden, terrace, balcony, outdoor patio with sink and gas grill (summer kitchen), billiards
- Fully equipped kitchen, fridge, dishwasher, coffee machine, flat-screen TV, A/C, free Wi-Fi, free private parking, towels and bed linen
- Views: sea, pool, garden, courtyard
- Check-in 16:00–22:00 (tell the host your arrival time), check-out 07:00–10:00. €500 cash damage deposit, refunded after inspection. Minimum check-in age 26. Children of all ages, free cot 0–2 on request, no extra beds. No smoking, no parties, no pets.
- Distances (host text): Opatija 7 km, Ičići beach 4 km, first grocery store 150 m, Bistro Bussola / Restaurant Lučica / Restaurant Galeb 4 km. Lovran old town 6.9 km (Booking). Booking's OSM line for Ičići beach says 2.1 km (straight line); the site uses the host's 4 km.
- Coordinates 45.3188963, 14.2708245
- Score 10 "Exceptional" from 2 reviews; categories 10 except location 8.8. Booking.com quality rating 4/5.
- Davorowski Holiday Homes is no longer mentioned on the site (owner request, 3 Nov 2026).
- Spelling: Booking writes "Ziganto"; the facade sign and the host text say **"Villa Žiganto"** — the site uses Žiganto.

## Unverified — not claimed on the site, confirm with the owner

- **Maximum guests.** Booking says max 4 adults, but there are beds for 8 + a sofa bed. The site gives no guest count (the inquiry form allows up to 8 adults — adjust when confirmed).
- **Saltwater pool.** Only the Booking URL slug says "with-saltwater-pool"; not mentioned on the site.
- Pool size, heating, season dates.
- Washing machine/dryer are visible in the games-room photo but not listed by Booking — not mentioned.
- Tennis court and fishing appear in Booking's generic "activities" list — not mentioned.
- Prices: the 2027 June week showed €5,243 for 4 adults; the site shows no prices.
- Direct contact (from the owner, 3 Nov 2026): +385 98 297 179, arnold.ziganto@gmail.com — shown in the hero, inquiry card, footer, mobile bar and JSON-LD. Owner is elderly and not tech-savvy — keep everything on WhatsApp/phone.

## Photo map (MyLuxoria page order → file)

ml01 garden-olive · ml02 villa-pool (hero, outdoors, og-image) · ml03 pool-edge (location) · ml04 pool-shower (day 10:00, outdoors, inquiry bg) · ml06 balcony-view (intro, day 08:00) · ml07 exterior-pool (intro) · ml08 living-sofa · ml09 living-tv · ml10 hall-stairs · ml11 kitchen-dining · ml12 dining-kitchen · ml13 bath-round · ml14 bedroom-print (bedroom 3) · ml15 bedroom-blue (bedroom 4) · ml16 bath-shelf · ml17/18 bedroom-leopard(-art) (gallery only) · ml19 bath-shower · ml20 bedroom-rose-view (bedroom 1) · ml21 bedroom-rose · ml22 bedroom-grey-view (bedroom 2) · ml23 bedroom-grey · ml24 bath-wood · ml25 jacuzzi-view · ml26 jacuzzi-room · ml27 terrace-lounge · ml28 pergola-dining (day 13:00, outdoors) · ml29 summer-kitchen · ml30 grill-table (kitchen block, day 19:30) · ml31 pool-garden.
ml05 = duplicate of ml01, not used. Portrait photos: bath-*, bedroom-leopard, pergola-dining (frames crop them with object-fit).

Note: the photos show five differently styled bedrooms (ml14, ml17/18, ml20/21, ml22/23, ml15) while Booking lists four — confirm with the owner.
