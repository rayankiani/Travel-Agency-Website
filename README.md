# Wanderlust Travels - Travel Agency Website

A modern, responsive single-page travel agency website built with HTML, Tailwind CSS (CDN), custom CSS, and vanilla JavaScript.

## Project Overview

This project is a front-end landing page for a fictional travel brand, **Wanderlust Travels**. It showcases destinations, travel packages, services, testimonials, an image gallery with lightbox, and inquiry/newsletter forms.

## Live Features

- Responsive navigation with desktop links and animated mobile slide-in menu
- Hero section with gradient typography, typing animation, and parallax background effect
- Destination showcase cards with hover motion and ratings
- Package pricing cards with call-to-action buttons
- Services section with icon-based feature cards
- About/statistics section with animated counters
- Gallery section with clickable image lightbox
- Testimonials carousel with autoplay, arrows, and dot navigation
- Booking form with client-side required-field validation
- Newsletter form with client-side submit handling
- Scroll reveal animations via `IntersectionObserver`
- Smooth anchor scrolling with navbar offset handling
- Loading screen shown briefly on initial page load
- Ripple click effect for CTA buttons

## Tech Stack

- **HTML5** for structure (`index.html`)
- **Tailwind CSS (CDN)** for utility-first styling and layout
- **Custom CSS** in `style.css` for advanced effects/animations
- **Vanilla JavaScript** in `script.js` for UI interactivity
- **Font Awesome 6.4.0 (CDN)** for icons
- **Google Fonts**: Playfair Display, Poppins

## Project Structure

```text
Travel-Agency-Website/
|- index.html
|- style.css
|- script.js
|- images/
|  |- hero-bg.jpg
|  |- destination-santorini.jpg
|  |- destination-bali.jpg
|  |- destination-switzerland.jpg
|  |- destination-tokyo.jpg
|  |- destination-paris.jpg
|  |- destination-maldives.jpg
|  |- gallery-1.jpg ... gallery-6.jpg
|  |- testimonial-1.jpg ... testimonial-3.jpg
```

## Page Sections

The single-page navigation links to these section IDs:

- `#home`
- `#destinations`
- `#packages`
- `#services`
- `#about`
- `#gallery`
- `#testimonials`
- `#booking`
- `#contact`

## JavaScript Functionality (`script.js`)

- `window.load` event hides loader after ~1 second.
- Navbar scroll listener adds/removes blur/shadow/solid background state.
- Mobile menu controls:
  - Open/close actions (`hamburger`, `closeMenu`, overlay click)
  - Auto-close when a mobile link is clicked
  - Locks body scrolling while menu is open
- Scroll reveal observer animates `.reveal` elements when in viewport.
- Counter observer animates `.counter` from `0` to each `data-target` value.
- Testimonials:
  - `showSlide(index)`
  - `nextSlide()` / `prevSlide()`
  - `goToSlide(index)`
  - Auto-advances every 5 seconds
- Lightbox:
  - `openLightbox(src)`
  - `closeLightbox()`
  - Escape key closes modal
- Booking form (`#bookingForm`): validates required fields and shows alert feedback.
- Newsletter form (`#newsletterForm`): shows alert feedback and resets input.
- Smooth scrolling for in-page anchor links with fixed navbar offset.
- Hero typing effect animates the text "With Us".
- Parallax effect updates hero background Y-position on scroll.
- Button ripple effect injects temporary animated spans on click.

## CSS Highlights (`style.css`)

- CSS custom properties for gradients and glassmorphism tokens
- Custom scrollbar styling
- Hero fixed-background parallax behavior
- Glass and glass-dark utility classes
- Gradient text rendering utility
- Animated nav underline on hover
- Card hover transforms for destinations/packages/features
- Gallery overlay + centered icon reveal
- Lightbox modal layout and zoom-in animation
- Testimonial fade state transitions
- Input focus transitions and glow
- Loader spinner animation
- Reveal animation classes
- Mobile menu, overlay, and hamburger icon animations
- Typing cursor blink animation

## Forms Included

### Booking Form (`#bookingForm`)

Fields:

- `name` (text, required)
- `email` (email, required)
- `phone` (tel, required)
- `destination` (select, required)
- `date` (date, required)
- `guests` (number, required, 1-20)
- `message` (textarea, optional)

Current behavior:

- Prevents default submission
- Validates required fields on the client
- Adds red border to invalid fields
- Displays success/error alerts
- Resets form on success

### Newsletter Form (`#newsletterForm`)

Fields:

- `email` (required)

Current behavior:

- Prevents default submission
- Displays a subscription success alert
- Resets input

## External Dependencies (CDN)

Defined in `index.html`:

- Tailwind CSS: `https://cdn.tailwindcss.com`
- Font Awesome: `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css`
- Google Fonts:
  - `Playfair Display`
  - `Poppins`

> Note: Because dependencies are loaded from CDNs, internet access is required for full styling and icons.

## How to Run Locally

1. Clone or download this project.
2. Open the project folder.
3. Open `index.html` directly in your browser.

Optional (recommended) local server methods:

- VS Code Live Server extension
- Python:

```bash
python -m http.server 5500
```

Then open: `http://localhost:5500`

## Browser Compatibility

Best experience on modern browsers supporting:

- `IntersectionObserver`
- `classList`
- CSS backdrop filters / transforms / animations
- ES6+ JavaScript features

Recent Chrome, Edge, Firefox, and Safari versions are recommended.

## Customization Guide

### Branding

- Website title, meta description, and brand name: edit `index.html`
- Logo icon and text in navbar/footer: edit `index.html`

### Colors and Theme

- Tailwind extended palette is defined in the inline `tailwind.config` block in `index.html`
- Custom CSS variables are in `:root` inside `style.css`

### Content

- Destinations, package pricing, testimonials, and contact details are all editable directly in `index.html`
- Replace images inside `images/` while keeping the same filenames, or update paths in `index.html`

### Interactions

- Update animation timing/behavior in `script.js`
- Update hover/transition visual style in `style.css`

## Important Notes

- This is a static front-end project. Forms are not connected to any backend service.
- Alert popups are placeholders for real UX patterns (toasts/modals) and backend responses.
- Tailwind is used via CDN, not a build pipeline.

## Suggested Next Improvements

- Connect booking/newsletter forms to a backend or service (Node, Firebase, Formspree, etc.)
- Add server-side validation and spam protection (reCAPTCHA/honeypot)
- Add SEO/social tags (Open Graph, Twitter card, canonical URLs)
- Improve accessibility (focus trapping for lightbox, ARIA labels, form error messaging)
- Add performance optimizations (image compression/lazy loading strategy)
- Add automated formatting/linting and optional build pipeline

## Author

Project: **Wanderlust Travels - Travel Agency Website**

If you want, this README can be extended further with deployment steps for GitHub Pages, Netlify, and Vercel.
