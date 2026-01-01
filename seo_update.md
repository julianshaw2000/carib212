COPILOT PROMPT (Cursor / GitHub Copilot Chat)

Goal: Update carib212.com homepage SEO + Airbnb links so Google shows “Ocho Rios Airbnb” and social shares look correct. Focus keyword: Ocho Rios Airbnb.

Context:
- Single static HTML file (shown below) using Tailwind CDN.
- Current <title> is “Carib212 Apartment Rental”.
- There are 2 Airbnb links using a placeholder “your-room-id”.
- Real Airbnb URL: https://www.airbnb.com/rooms/44134587?source_impression_id=p3_1614918663_1U86TPLw9DkawtLH&guests=1&adults=1

Make these edits:

1) Update the document title tag
- Replace:
  <title>Carib212 Apartment Rental</title>
- With:
  <title>Ocho Rios Airbnb – Oceanfront 1-Bed Condo | Carib212</title>
- Keep title length reasonable (~50–60 chars). Don’t add extra words.

2) Add SEO meta tags in <head> (directly under <title>)
Add:
- meta description using the focus keyword “Ocho Rios Airbnb”
- canonical link to https://carib212.com/
- Open Graph tags for WhatsApp/Facebook previews:
  og:type, og:title, og:description, og:url, og:image
- Twitter card tags:
  twitter:card, twitter:title, twitter:description, twitter:image
Rules:
- Use og:url matching canonical.
- Use og:image as an absolute URL: https://carib212.com/images/overview.jpg
- Keep descriptions short, plain language.

3) Replace the Airbnb links in BOTH locations
- In the nav Airbnb icon link
- In the “Book on Airbnb” button
Replace the href with the exact Airbnb URL above.
Also:
- Keep target="_blank" and rel="noopener"
- Remove the query params “guests=1&adults=1” ONLY if you judge it safer/cleaner; otherwise leave as provided. Don’t break the link.

4) Add a matching H1 for on-page relevance (optional but recommended)
- Current H1: “Find Your Perfect Stay”
Change it to include the focus keyword:
  “Ocho Rios Airbnb – Carib212 Oceanfront Condo”
Keep it readable for humans.

5) Add Lodging schema JSON-LD in <head> (below meta tags)
Insert a script tag:
- @context: https://schema.org
- @type: LodgingBusiness (or VacationRental if you think better supported)
- name: “Carib212 – Oceanfront 1BR Condo”
- url: https://carib212.com/
- image: https://carib212.com/images/overview.jpg
- address: locality Ocho Rios, region Saint Ann, country JM
Don’t invent street address.

6) Output
- Provide the final updated <head> section in full (copy/paste ready).
- Provide a diff-like summary listing exactly what lines changed (no long explanation).
- Ensure HTML remains valid.

Here is the file to modify:
(paste the full HTML file content from my message verbatim and apply the changes)
