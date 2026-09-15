# THE भु-से-छो:

**DRIFT. EAT. PLAY. REPEAT.**

The website for **THE भु-से-छो:** — a restaurant, chulo kitchen, RC drift space, family hangout, and live-music venue in School Dada, Urlabari-4, Morang, Nepal.

This repository contains the frontend for the restaurant's main website and its interactive online menu/order experience.

[![Live Site](https://img.shields.io/badge/live-vusechho.vercel.app-1A1714?style=flat-square)](https://vusechho.vercel.app/)
[![Source](https://img.shields.io/badge/source-GitHub-1A1714?style=flat-square)](https://github.com/iamlaxman/vusechho-restro)
[![HTML](https://img.shields.io/badge/built%20with-HTML%2FCSS%2FJS-E8590C?style=flat-square)](https://github.com/iamlaxman/vusechho-restro)
[![Vercel](https://img.shields.io/badge/deployed-Vercel-black?style=flat-square)](https://vercel.com/)

---

## About

THE भु-से-छो: is built around more than food.

The website presents the place as a complete experience:

```text
CHULO KITCHEN
      +
FOOD
      +
RC DRIFT
      +
PLAY
      +
LIVE MUSIC
      +
PEOPLE
```

The homepage is therefore designed more like an editorial experience than a conventional restaurant template.

The digital menu then switches from storytelling to a practical ordering interface.

---

## Website

**Live:**
https://vusechho.vercel.app/

**Repository:**
https://github.com/iamlaxman/vusechho-restro

---

# Homepage

The main `index.html` contains the complete restaurant experience.

The navigation is organized around:

```text
01  Experience
02  Menu
03  Drift
04  Live
05  Gallery
06  Find Us
      +
    Order Now
```

The navigation appears after the hero and has a dedicated fullscreen mobile menu.

---

## Hero

The homepage opens with a full-screen hero built around the restaurant identity.

The current headline is:

> A plate of love, from Nepali fire for you.

The hero includes:

* THE भु-से-छो: identity
* Urlabari / Morang location marker
* Nepali typography
* animated hand-drawn squiggle
* large thali artwork
* Order Now CTA
* View Menu CTA
* 4.5 rating / 521 Google reviews presentation

The primary `Order Now` button goes directly to `menu.html`.

---

# Manifesto

Immediately after the hero, the site introduces the idea behind the venue:

> Come for the food. Stay for everything else.

The section describes THE भु-से-छो: as a combination of a chulo kitchen, drift track, stage, and table rather than only a restaurant.

---

# Experience

The Experience section is divided into four panels:

```text
01 / EAT
02 / DRIFT
03 / PLAY
04 / LIVE
```

### Eat

Food from the chulo to the table, with an emphasis on smoke, spice, shared plates, and open-fire cooking.

### Drift

RC racing with fast corners and friendly competition.

### Play

A space aimed at families, kids, groups, and people who simply want to spend time there.

### Live

Live music and local performances that turn dinner into an evening experience.

These four experiences are implemented as individual cards on the homepage.

---

# Menu Showcase

The homepage has its own interactive menu showcase.

It does **not** display the complete menu.

Instead, it presents four selected dishes:

```text
01 — Chef's Pick
VUSE Chicken Khana
Rs. 300

02 — Dumplings
Chicken Jhol Momo
Rs. 180

03 — Charred
Chicken Chhoila
Rs. 290

04 — Grilled
Chicken Sekuwa
Rs. 200
```

Each dish has:

* image
* description
* tags
* price
* category-style label

Selecting a thumbnail morphs the main card and image into the selected dish using JavaScript transitions.

The section ends with:

```text
View full menu & order
```

which links to `menu.html`.

---

# Drift

The Drift section is one of the more technically interesting parts of the homepage.

It uses a Vimeo video as the background visual.

The implementation:

* shows a poster image first
* injects the Vimeo iframe after the page becomes interactive
* starts the video around 19 seconds
* loops the 19–60 second segment
* loads the Vimeo Player API after the video is ready
* pauses the player when the Drift section leaves the viewport
* resumes playback when it comes back
* avoids loading the animated video when reduced motion is requested

This is implemented directly in the page's JavaScript rather than through a frontend framework.

The section also presents:

```text
3       Track layouts
14m     Lap length
All     Skill levels
```

and includes an order/pickup CTA.

---

# Play

The Play section makes it clear that the venue isn't intended only for RC racers.

It presents:

* family tables
* outdoor space
* group seating
* kid-friendly space

The content is aimed at people who want to eat, hang out, or spend time at the venue without necessarily participating in RC racing.

---

# Live

The Live section focuses on the venue's music and events.

The current page presents:

```text
Weekly       Live sets
FRI · 19:00

Monthly      Drift nights
SAT · 18:00

Private      Private events
On request
```

It also uses a dedicated music image.

---

# Gallery

The homepage contains an image gallery showing different sides of the venue.

The desktop presentation includes panels for:

```text
01  Table
02  Track
03  Chulo
04  Drift
```

The mobile version turns the gallery into a touch-friendly slider with:

* swipe gestures
* previous/next buttons
* pagination dots
* keyboard navigation

The mobile gallery implementation is handled directly with JavaScript and touch events.

---

# Reviews

The homepage also contains a restaurant review section using individual review cards and Google-review presentation.

The hero currently displays:

```text
★★★★★
4.5 · 521 Google reviews
```

as part of the site's social-proof presentation.

---

# Find Us

The location section provides:

```text
School Dada
Urlabari-4
Morang, Nepal

Open daily
10:00 — 22:00
```

It includes:

* Get Directions button
* Google Maps link
* embedded Google Map

The coordinates and map are also represented in the site's structured data.

---

# Digital Menu

`menu.html` is not just a static menu page.

It is a complete client-side menu browsing and ordering interface.

The page contains:

```text
Menu
 │
 ├── Search
 │
 ├── Categories
 │
 ├── Category banner
 │
 ├── Food items
 │
 ├── Cart
 │
 └── Checkout
```

---

## Menu Hero

The menu opens with:

> Cooked over fire, served fresh to your door.

The description specifically mentions:

* momo
* sekuwa
* thukpa
* biryani
* chowmein
* chulo cooking
* delivery inside Urlabari

The page currently advertises:

```text
87+ Dishes
12 Categories
```

as its menu statistics.

---

# Menu Categories

The menu data is defined directly in `menu.html` as JavaScript data.

Categories include food groups such as:

* Momo
* Sekuwa & Grills
* Khaja
* Biryani
* Noodles
* Soup
* Thali
* Breakfast
* Tea
* Fried Rice
* Roti
* Vegetarian

The implementation also defines category icons and individual category banner imagery/descriptions.

The complete menu is rendered dynamically from the `CATEGORIES` data structure.

---

# Food Items

Each menu item contains structured information including:

```javascript
{
  name: "...",
  price: 200,
  veg: false,
  off: 0
}
```

This allows the interface to automatically handle:

* item name
* price
* vegetarian status
* non-vegetarian status
* discounts

The UI calculates the original price when a discount is present and displays the discount percentage.

---

# Search

The menu has live product search.

Typing into the search field immediately re-renders the menu items.

Search matches against:

* item names
* category names

If nothing matches, the interface displays an empty state rather than leaving the page blank.

---

# Cart

The cart is fully client-side.

Customers can:

* add items
* increase quantities
* decrease quantities
* remove items
* clear the cart
* view total item count
* view subtotal
* open a dedicated order/cart page

The cart uses JavaScript state rather than a database.

Each item is keyed by its category and name.

---

# Checkout

The checkout is implemented as a modal.

The customer provides:

```text
Name
Phone
Delivery address
Notes
```

The system only accepts delivery addresses that match configured Urlabari-related keywords.

The current configuration includes locations such as:

```text
Urlabari
School Dada
Urlabari Bazar
Urlabari Chowk
Urlabari-1
Urlabari-2
...
Urlabari-9
```

The checkout therefore intentionally limits online delivery to Urlabari.

---

# Payment

The checkout supports two payment paths:

### Cash on Delivery

The customer can select Cash on Delivery.

### QR Payment

The interface provides a QR-payment section intended for:

```text
Fonepay
eSewa
Khalti
```

The customer is shown the calculated amount and can enter a payment/reference ID.

The QR image is configurable through:

```javascript
CONFIG.qrImage
```

and is currently empty in the repository configuration.

---

# Order Submission

The current ordering system does **not** send the order to a restaurant backend or database.

Instead, the browser creates a formatted WhatsApp message containing:

```text
Customer
Phone
Address
Payment method
Reference ID
Notes
Order items
Subtotal
Delivery / COD
Total
```

and opens WhatsApp using the restaurant's configured WhatsApp number.

The current configuration uses:

```text
+977 986-5599528
```

for the WhatsApp order destination.

The actual submission flow is:

```text
Customer
   ↓
Cart
   ↓
Checkout
   ↓
Validation
   ↓
Build WhatsApp message
   ↓
Open WhatsApp
   ↓
Restaurant receives order
```

This is important: **the current repository does not contain a real order backend.**

---

# Order Confirmation

After opening WhatsApp, the frontend generates a random six-digit-style order number and displays a local success screen.

The confirmation message tells the customer that the order has been received and that confirmation will follow through WhatsApp.

The cart is then cleared on the client side.

This confirmation is therefore a **frontend confirmation state**, not proof that a server successfully created or stored an order.

---

# Visual System

The site deliberately uses a strong editorial / restaurant identity instead of a conventional template.

The main design tokens include:

```text
Ink
Paper
Clay
Moss
```

with the primary clay accent:

```text
#E8590C
```

The homepage uses:

* dark ink backgrounds
* warm paper surfaces
* clay-orange accents
* strong borders
* editorial serif typography
* monospace metadata
* Nepali Devanagari typography
* large display type
* image-led sections

The core fonts include:

```text
Fraunces
Instrument Serif
Inter
IBM Plex Mono
Noto Sans Devanagari
```

These are defined directly in the homepage stylesheet.

---

# Motion

Motion is an important part of the implementation.

The homepage includes:

* hero entrance animation
* fade-up reveals
* SVG squiggle drawing
* menu-card morphing
* image transitions
* mobile menu transitions
* smooth scrolling
* Vimeo video playback
* gallery sliding
* IntersectionObserver-based section reveals

The site also checks:

```javascript
window.matchMedia('(prefers-reduced-motion: reduce)')
```

and changes behaviour accordingly.

---

# Accessibility

The pages include several accessibility-oriented details:

* semantic headings
* labelled navigation
* ARIA labels
* keyboard interaction
* focus-visible styling
* skip link
* dialog roles
* tab roles for interactive menu selectors
* keyboard gallery controls
* reduced-motion handling

The menu also supports keyboard interaction for several controls and uses accessible labels for food and cart actions.

---

# SEO

The homepage includes a fairly extensive SEO implementation.

It provides:

* title
* description
* canonical URL
* Open Graph metadata
* Twitter metadata
* geographic metadata
* restaurant Schema.org data
* menu structured data
* robots configuration
* sitemap
* PWA metadata

The structured restaurant information includes:

```text
THE भु-से-छो:
Urlabari, Morang
Nepal
NPR 100–2000
10:00–22:00
```

along with cuisine, payment methods, phone number, menu URL, coordinates, and map information.

---

# PWA

The project includes PWA-related assets:

```text
favicon/
├── favicon.ico
├── favicon.svg
├── favicon-96x96.png
├── apple-touch-icon.png
└── site.webmanifest
```

The homepage references the manifest and mobile web-app metadata.

---

# Technology

The project deliberately keeps the frontend simple.

### Core

* HTML5
* CSS3
* Vanilla JavaScript
* SVG
* Web APIs

### External services/resources

* Google Fonts
* Vimeo
* Google Maps
* external food/photography image resources
* WhatsApp

There is currently no React, Vue, Angular, Next.js, or other frontend framework.

---

# Project Structure

```text
vusechho-restro/
│
├── index.html
├── menu.html
├── menu-demo.html
├── demo-index.html
│
├── 404.html
├── 500.html
│
├── logo.png
├── thali.png
├── og-image.jpg
├── footer-lines.png
│
├── assets/
│   └── images/
│       ├── people.jpg
│       ├── track.jpg
│       ├── drift.jpg
│       └── music.jpg
│
├── favicon/
│   ├── favicon.ico
│   ├── favicon.svg
│   ├── favicon-96x96.png
│   ├── apple-touch-icon.png
│   └── site.webmanifest
│
├── robots.txt
├── sitemap.xml
├── security.txt
├── humans.txt
├── llms.txt
│
├── google52bc1746b00ad660.html
└── vercel.json
```

---

# Local Development

Clone the repository:

```bash
git clone https://github.com/iamlaxman/vusechho-restro.git
cd vusechho-restro
```

No frontend build process is required.

Run a local HTTP server:

```bash
python3 -m http.server 8080
```

Then visit:

```text
http://localhost:8080
```

A local server is recommended instead of opening the HTML files directly because the site uses external resources, media, and browser APIs.

---

# Deployment

The project is deployed on Vercel.

Because the application is primarily static HTML/CSS/JavaScript, it does not require a traditional frontend build pipeline.

The repository contains:

```text
vercel.json
```

for deployment configuration.

---

# Current Ordering Architecture

The current implementation is intentionally simple:

```text
                  CUSTOMER
                     │
                     ▼
                menu.html
                     │
              Browse / Search
                     │
                     ▼
                   Cart
                     │
                     ▼
                 Checkout
                     │
          ┌──────────┴──────────┐
          │                     │
        Cash                  QR Pay
          │                     │
          └──────────┬──────────┘
                     │
                     ▼
              Client validation
                     │
                     ▼
             WhatsApp message
                     │
                     ▼
             Restaurant WhatsApp
```

There is no database-backed order state in the current `menu.html` implementation.

---

# Future Restaurant System

The frontend can later be extended into a complete restaurant ordering system.

A production architecture could become:

```text
QR TABLE
   │
   ▼
MENU
   │
   ▼
CART
   │
   ▼
ORDER API
   │
   ├──────────► WAITER
   │
   ├──────────► KITCHEN
   │
   └──────────► CUSTOMER
                    │
                    ▼
                  BILL
                    │
                    ▼
                 CASHIER
                    │
                    ▼
             TABLE RELEASED
```

Possible additions include:

* table-specific QR codes
* real-time order status
* kitchen display
* waiter dashboard
* cashier dashboard
* digital bills
* bill printing
* table locking
* order history
* menu management
* staff authentication
* payment verification
* backend order storage

Those features are **not part of the current static repository**.

---

# Roadmap

* [ ] Move menu data into a central data source
* [ ] Add real backend order processing
* [ ] Add table QR ordering
* [ ] Add waiter dashboard
* [ ] Add kitchen dashboard
* [ ] Add cashier interface
* [ ] Add digital billing
* [ ] Add printable bills
* [ ] Add table status management
* [ ] Add order status tracking
* [ ] Add proper payment verification
* [ ] Add order persistence
* [ ] Improve menu administration
* [ ] Optimize external image dependencies
* [ ] Add automated accessibility checks
* [ ] Add automated frontend testing

---

# Design Philosophy

The website should feel like THE भु-से-छो:, not like a restaurant website purchased from a template marketplace.

That means:

```text
Food before decoration.

Character before convention.

Motion with purpose.

Mobile before desktop assumptions.

Simple technology where simple technology works.
```

The homepage tells the story.

The menu gets the customer to the food.

The ordering flow gets the order to the restaurant.

---

# Author

**Laxman Poudel**

GitHub:
https://github.com/iamlaxman

Website:
https://laxman-poudel.com.np/

---

<p align="center">
  THE भु-से-छो: · Urlabari, Morang · Nepal
</p>

<p align="center">
  <a href="https://vusechho.vercel.app/">Visit Website</a>
  ·
  <a href="https://github.com/iamlaxman/vusechho-restro">Source Code</a>
</p>
