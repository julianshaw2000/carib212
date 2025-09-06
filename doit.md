Objective: Create a clean, elegant, and responsive single-page website for an Airbnb-style apartment rental. The design should be responsive and heavily focused on high-quality images, using Tailwind CSS for all styling.

Technology Stack:

HTML5

Tailwind CSS (via CDN)

Vanilla JavaScript

Structure & Styling Requirements:

1. HTML Structure:

Create a single index.html file.

Include the Tailwind CSS CDN link in the <head> of the document: <script src="https://cdn.tailwindcss.com"></script>.

Place all JavaScript within a <script> block before the closing </body> tag.

The main structure should consist of a <header>, a <main>, and a <footer>.

2. Tailwind CSS Styling:

General: Use utility classes for a soft off-white background (bg-gray-50), a deep charcoal for text (text-gray-800), and a subtle accent color of your choice (e.g., text-teal-500, bg-teal-500). Use spacing classes like p-16 or my-12.

Hero Section (<header>):

Use classes like h-screen w-full relative for the full-screen container.

Use a background image class or inline style with bg-cover bg-center.

For the navigation bar, use bg-opacity-40 on a background color class to create the transparency effect (e.g., bg-white bg-opacity-40).

Center the call-to-action button using Flexbox classes (flex items-center justify-center).

Adventures Section:

Use CSS Grid classes like grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 for a responsive card layout.

Use rounded-lg shadow-lg overflow-hidden for card styling.

Apartment Carousel Section:

Create a container with relative positioning.

Use classes for a full-width image and positioning for navigation buttons (absolute inset-y-0 left-0 and absolute inset-y-0 right-0).

Use object-cover on all image elements.

Booking Section:

Create a simple container using spacing and background classes.

Use text-center for alignment and p-8 for padding.

3. JavaScript Functionality:

Image Carousel:

Write a script that handles the carousel functionality.

Implement event listeners for the "Previous" and "Next" buttons to change the active image. The images should be a simple array.

Smooth Scrolling:

Add a script to enable smooth scrolling when clicking on navigation links that point to different sections (e.g., #adventures-section).

4. Placeholder Content:

Images: Use placeholder image URLs (e.g., https://picsum.photos/1920/1080?random=1).

Text:

Hero button: "Find Your Next Adventure"

Adventures: "Blue Hole," "Dunn's River Falls," "Chukka Park Rides" with a one-sentence description for each.

Booking section: "Book Your Stay," and the placeholder <div> with ID stripe-payment-form-container.

Final Instruction to Copilot:
"Generate the complete, single index.html file with the Tailwind CSS CDN link and the JavaScript embedded. Use appropriate Tailwind classes for all styling. Add clear comments to explain each section of the code."