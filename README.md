<div align="center">

<img src="https://vusechho.vercel.app/favicon/favicon.svg" alt="THE भु-से-छो: logo" width="120">

# THE भु-से-छो:

### DRIFT. EAT. PLAY. REPEAT.

**A restaurant, chulo kitchen, RC drift space, and live-music experience in Urlabari, Morang, Nepal.**

<br>

[![Live Site](https://img.shields.io/badge/live-vusechho.vercel.app-1A1714?style=flat-square)](https://vusechho.vercel.app/)
[![Source](https://img.shields.io/badge/source-GitHub-1A1714?style=flat-square)](https://github.com/iamlaxman/vusechho-restro)
[![Built with](https://img.shields.io/badge/built%20with-HTML%20%2F%20CSS%20%2F%20JS-E8590C?style=flat-square)](https://github.com/iamlaxman/vusechho-restro)
[![Vercel](https://img.shields.io/badge/deployed-Vercel-black?style=flat-square)](https://vusechho.vercel.app/)

</div>

---

## About

THE भु-से-छो: is built around more than food.

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

The website brings those experiences together in one place.

The homepage is designed as an immersive restaurant experience, while the separate menu provides a practical food-browsing and ordering interface.

---

## Website

**Live:** https://vusechho.vercel.app/

**Repository:** https://github.com/iamlaxman/vusechho-restro

---

## Homepage

`index.html` is the main experience layer of the website.

It includes:

* full-screen hero
* restaurant introduction
* Experience section
* Eat / Drift / Play / Live cards
* interactive featured menu
* RC Drift section
* Vimeo background video
* Play section
* Live events
* image gallery
* reviews
* Find Us / Google Maps
* responsive navigation
* mobile menu
* Order Now / View Menu CTAs

The visual direction is deliberately editorial and tactile rather than following a conventional restaurant template.

---

## Menu

`menu.html` is the functional digital menu.

It includes:

* 87+ dishes
* 12 food categories
* menu search
* category filtering
* vegetarian / non-vegetarian indicators
* discounted prices
* food cards
* cart
* quantity controls
* checkout modal
* customer information
* delivery address validation
* Cash on Delivery
* QR payment option
* payment reference field
* WhatsApp order submission
* client-side order confirmation

The current order flow is:

```text
MENU
  ↓
SEARCH / CATEGORY
  ↓
FOOD ITEM
  ↓
ADD TO CART
  ↓
CHECKOUT
  ↓
VALIDATION
  ↓
PAYMENT OPTION
  ↓
WHATSAPP ORDER
```

The current implementation is client-side and does **not** use a database-backed order-management backend.

---

## Logo

The website uses the project's favicon as its primary compact logo asset:

<img src="https://vusechho.vercel.app/favicon/favicon.svg" alt="THE भु-से-छो: logo" width="80">

Source:

https://vusechho.vercel.app/favicon/favicon.svg

---

## Technology

* HTML5
* CSS3
* Vanilla JavaScript
* SVG
* Google Fonts
* Vimeo
* Google Maps
* WhatsApp
* Vercel

No React, Vue, Angular, Next.js, or other frontend framework is required.

---

## Project Structure

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

## Local Development

```bash
git clone https://github.com/iamlaxman/vusechho-restro.git
cd vusechho-restro
```

Run a local server:

```bash
python3 -m http.server 8080
```

Open:

```text
http://localhost:8080
```

No build step is required.

---

## Deployment

The site is deployed through Vercel.

The project is primarily static HTML, CSS, JavaScript, and assets, so it can also be served from other static hosting platforms.

---

## Location

**THE भु-से-छो:**

School Dada
Urlabari-4
Morang, Nepal

**Opening hours:**
10:00 — 22:00

---

## Design Philosophy

The website is built around a few simple ideas:

```text
FOOD FIRST

CHARACTER OVER TEMPLATE

MOTION WITH PURPOSE

MOBILE MATTERS

KEEP THE STACK SMALL
```

The goal is not to make another polished-looking restaurant template.

It should feel like the place itself — warm, energetic, local, slightly rough around the edges, and built around food and experience.

---

## Roadmap

* [ ] Real backend ordering
* [ ] QR-based table ordering
* [ ] Real-time waiter orders
* [ ] Kitchen display
* [ ] Cashier dashboard
* [ ] Digital bills
* [ ] Printable bills
* [ ] Table status management
* [ ] Order history
* [ ] Menu management
* [ ] Payment verification
* [ ] Staff authentication
* [ ] Centralized menu data
* [ ] Automated testing
* [ ] Accessibility improvements

---

## Author

**Laxman Poudel**

[GitHub](https://github.com/iamlaxman)

---

<div align="center">

<img src="https://vusechho.vercel.app/favicon/favicon.svg" alt="THE भु-से-छो:" width="50">

**THE भु-से-छो:**

Urlabari, Morang · Nepal

[Visit Website](https://vusechho.vercel.app/) · [View Source](https://github.com/iamlaxman/vusechho-restro)

</div>
