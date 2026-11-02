You are editing a single static file: index.html for Carib212.com (Tailwind CDN site).
Apply the following changes precisely. Keep everything else as-is (Stripe buttons, hero, images, etc.).

GOALS
1) Add a “Local Guide” section with cards (breakfast, market, vegan ice cream, secluded beach, dining, live reggae) using Tailwind.
2) Replace the Evita dining card with “Ciao Bella Art Cafe & Restaurant”.
3) Add “Local Guide” to both desktop and mobile navs.
4) Fix JSON-LD (remove the inline JS comment).
5) Remove accidental duplicate HTML document appended at the end of the file.
6) (Optional tidy) De-duplicate the carousel image list where exact duplicates appear.

DETAILS

A) NAV LINKS
- In the desktop nav list `<ul class="hidden md:flex gap-8">…</ul>` add:
  `<li><a href="#local-guide" class="hover:text-teal-300 text-white transition">Local Guide</a></li>`
- In the mobile menu list `<div id="mobile-menu" …>` add an equivalent link:
  `<a href="#local-guide" class="text-lg text-white hover:text-teal-300">Local Guide</a>`

B) JSON-LD FIX
- In the LodgingBusiness `amenityFeature` array, remove the JS comment at the end of the “Mahogany Beach” line. Change:
  `{"@type":"LocationFeatureSpecification","name":"Mahogany Beach","value":true} // Added beach feature`
  to exactly:
  `{"@type":"LocationFeatureSpecification","name":"Mahogany Beach","value":true}`

C) INSERT “LOCAL GUIDE” SECTION
- Insert the following section **inside `<main>`**, after the “Adventures Nearby” section and before “Our Apartment”:

<section id="local-guide" class="my-12 px-8">
  <h2 class="text-3xl font-bold text-teal-500 mb-2 text-center">Local Guide: Food, Beaches & Reggae</h2>
  <p class="text-center text-gray-600 mb-8">Julian’s on-the-ground picks around Ocho Rios</p>

  <!-- Breakfast + Market -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
    <article class="bg-white rounded-lg shadow overflow-hidden">
      <img src="https://static.wixstatic.com/media/7a7eb7_e4e7cf12fc294645814494d4d4e45d14~mv2.jpg/v1/fill/w_800,h_533,al_c,q_80/Miss%20T%27s0173.jpg" alt="Miss T’s Kitchen outdoor dining, Ocho Rios" class="w-full h-56 object-cover">
      <div class="p-5">
        <h3 class="text-xl font-semibold mb-1">Miss T’s Kitchen</h3>
        <p class="text-gray-600 mb-3">Authentic Jamaican breakfast (also great for lunch &amp; dinner) in a lush yard setting.</p>
        <a href="https://maps.app.goo.gl/thSfXZENqYRfgYih6" target="_blank" rel="noopener" class="text-teal-600 hover:underline">Open in Google Maps →</a>
      </div>
    </article>

    <article class="bg-white rounded-lg shadow overflow-hidden">
      <img src="https://upload.wikimedia.org/wikipedia/commons/7/70/Farmers%27_market_in_Jamaica.jpg" alt="Farmers market produce in Jamaica" class="w-full h-56 object-cover">
      <div class="p-5">
        <h3 class="text-xl font-semibold mb-1">Saturday Farmers Market</h3>
        <p class="text-gray-600 mb-2">Laid-back market with fresh fruit, coconuts &amp; herbs. Best selection before <strong>1:00 PM</strong>.</p>
        <div class="flex flex-wrap gap-2 mb-3">
          <span class="text-xs bg-teal-50 text-teal-700 px-2 py-1 rounded-full">Fresh fruit</span>
          <span class="text-xs bg-teal-50 text-teal-700 px-2 py-1 rounded-full">Coconuts</span>
          <span class="text-xs bg-teal-50 text-teal-700 px-2 py-1 rounded-full">Herbal remedies</span>
        </div>
        <a href="https://maps.app.goo.gl/dsQyjhKZzUxQumyq6?g_st=ac" target="_blank" rel="noopener" class="text-teal-600 hover:underline">Open in Google Maps →</a>
      </div>
    </article>
  </div>

  <!-- Treats + Secluded Beach -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
    <article class="bg-white rounded-lg shadow overflow-hidden">
      <img src="https://images.unsplash.com/photo-1526318472351-c75fcf070305?q=80&amp;w=1200&amp;auto=format&amp;fit=crop" alt="Plant-based ice cream in a cup" class="w-full h-56 object-cover">
      <div class="p-5">
        <h3 class="text-xl font-semibold mb-1">Plant-Based Ice Cream</h3>
        <p class="text-gray-600 mb-3">Great vegan-friendly stop after the market.</p>
        <a href="https://maps.app.goo.gl/9CyaJK8yS277wjU38?g_st=aw" target="_blank" rel="noopener" class="text-teal-600 hover:underline">Open in Google Maps →</a>
      </div>
    </article>

    <article class="bg-white rounded-lg shadow overflow-hidden">
      <img src="https://upload.wikimedia.org/wikipedia/commons/0/08/JM-ocho_rios-hafen-01.jpg" alt="Ocho Rios coastline" class="w-full h-56 object-cover">
      <div class="p-5">
        <h3 class="text-xl font-semibold mb-1">Secluded Beach (Local Hideaway)</h3>
        <p class="text-gray-600 mb-3">Quiet spot away from the crowds — perfect for a chill swim.</p>
        <a href="https://maps.app.goo.gl/6ZQv7FE2eSoLZ6Zx5" target="_blank" rel="noopener" class="text-teal-600 hover:underline">Open in Google Maps →</a>
      </div>
    </article>
  </div>

  <!-- Dining -->
  <h3 class="text-2xl font-bold text-teal-500 mb-4">Dining</h3>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
    <!-- Ciao Bella (replaces Evita) -->
    <article class="bg-white rounded-lg shadow overflow-hidden">
      <img src="https://www.italianfoodjm.com/web/image/1375-b8eab317/juc.webp"
           alt="Ciao Bella Art Cafe &amp; Restaurant — coffee, pastries, fresh juice"
           class="w-full h-56 object-cover">
      <div class="p-5">
        <h4 class="text-lg font-semibold mb-1">Ciao Bella Art Cafe &amp; Restaurant</h4>
        <p class="text-gray-600 mb-3">Italian comfort food, brunch &amp; art vibe at Taj Mahal Plaza (central Ochi).</p>
        <a href="https://www.google.com/maps/search/?api=1&amp;query=Ciao+Bella+Art+Cafe+%26+Restaurant+Ocho+Rios"
           target="_blank" rel="noopener" class="text-teal-600 hover:underline">
          Open in Google Maps →
        </a>
      </div>
    </article>

    <article class="bg-white rounded-lg shadow overflow-hidden">
      <img src="https://www.margaritavillecaribbean.com/content/uploads/2017/07/ocho-exterior-beach-hut-190x110.jpg" alt="Margaritaville Ocho Rios exterior beach hut" class="w-full h-56 object-cover">
      <div class="p-5">
        <h4 class="text-lg font-semibold mb-1">Margaritaville Ocho Rios</h4>
        <p class="text-gray-600 mb-3">Beach-club vibe, pool &amp; nightlife. Tourist-friendly fun.</p>
        <a href="https://maps.app.goo.gl/gvA6b14och2jEozi6?g_st=aw" target="_blank" rel="noopener" class="text-teal-600 hover:underline">Open in Google Maps →</a>
      </div>
    </article>
  </div>

  <!-- Live Reggae & Nightlife -->
  <h3 class="text-2xl font-bold text-teal-500 mb-4">Live Reggae &amp; Nightlife</h3>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
    <article class="bg-white rounded-lg shadow overflow-hidden">
      <img src="https://connectingjamaica.com/wp-content/uploads/2025/03/oceans-11-a.jpg" alt="Ocean’s 11 meal and waterfront table" class="w-full h-56 object-cover">
      <div class="p-5">
        <h4 class="text-lg font-semibold mb-1">Ocean’s 11</h4>
        <p class="text-gray-600 mb-3">Local legend on the water — frequent live reggae &amp; karaoke nights.</p>
        <a href="https://maps.app.goo.gl/E73MYjyt2ZveB7e16?g_st=aw" target="_blank" rel="noopener" class="text-teal-600 hover:underline">Open in Google Maps →</a>
      </div>
    </article>

    <article class="bg-white rounded-lg shadow overflow-hidden">
      <img src="https://connectingjamaica.com/wp-content/uploads/2025/03/oceans-11-b-1.jpg" alt="Ocean’s 11 BBQ wings and salad" class="w-full h-56 object-cover">
      <div class="p-5">
        <h4 class="text-lg font-semibold mb-1">More Reggae Spots</h4>
        <p class="text-gray-600 mb-3">Ask Julian for what’s on this week — schedules change.</p>
        <a href="https://maps.app.goo.gl/E73MYjyt2ZveB7e16?g_st=aw" target="_blank" rel="noopener" class="text-teal-600 hover:underline">Open in Google Maps →</a>
      </div>
    </article>
  </div>

  <p class="text-xs text-gray-500 mt-6 text-center">
    Photo credits: Miss T’s Kitchen, Ciao Bella, Margaritaville Caribbean, ConnectingJamaica.com, Wikimedia Commons, Unsplash (ice cream).
    Schedules can change — check venue pages or call ahead.
  </p>
</section>

D) REMOVE DUPLICATE HTML
- At the bottom of the file there are repeated `</html>` blocks followed by a second full `<!DOCTYPE html>…</html>` document.
- Keep only the FIRST complete document. Delete all trailing duplicate HTML after the first closing `</html>`.

E) OPTIONAL TIDY: IMAGE ARRAY DEDUPE
- In the `apartmentImages` array, remove strict duplicates:
  - 'images/bathroom.avif' appears twice; keep one.
  - 'images/sundown.jpeg' appears twice; keep one.
- Maintain the rest of the order.

VALIDATION
- Ensure no JSON comments remain in `<script type="application/ld+json">`.
- Clicking “Local Guide” in both navs scrolls to `#local-guide`.
- Build/lint not required; this is a static file served with Tailwind CDN.
- No changes to Stripe buy buttons or their publishable keys.

Make these edits now and show me only the final, updated index.html content in your response.
