# MedRemind

MedRemind is a **static marketing/landing page** for a proposed medication-management app ("Scan. Schedule. Stay Healthy."). The page describes an idea: scanning doctor prescriptions, generating a medication schedule, and sending reminders through a voice assistant.

**Important: the app described on the page is not implemented in this repository.** This repo contains only the landing page. There is no prescription scanning, scheduling, reminder, notification, voice, or AI code here.

> **Disclaimer:** This project is a student demo. It is not medical advice and must not be used to manage real medication.

## Live demo

https://med-mind-phi.vercel.app (checked: HTTP 200). Note that the browser tab title of the page is "ForGood" (a leftover from a template), while the page heading is "MedRemind".

## What is actually implemented

- Single-page landing site with sections: Home, Services, Missions, About, Contact, and footer.
- Splash/intro animation on load (GSAP timeline in `js/script.js`).
- Responsive layout (Bootstrap 4 grid plus `css/responsive.css`).
- Image gallery in the "Missions" section with a click-to-enlarge popup (`js/script.js`).
- Navigation links that scroll to page sections.

## What is NOT implemented (only described in the page text)

- Prescription scanning / AI / OCR
- Medication schedules or reminders, voice or push notifications
- Weekly progress reports, health guides, nutrition plans
- Contact form: the fields have no handler and the "Submit Details" button is a placeholder link (`href="#"`); nothing is sent or stored.
- Social media links are placeholders (`href="#"`).
- There is no backend, database, or localStorage use. It is entirely front-end and static.

## Tech stack

- HTML, CSS, vanilla JavaScript
- Bootstrap 4.6.1, jQuery 3.5.1 (slim), Popper.js 1.16.1, Font Awesome 4.7.0, GSAP 3.12.5, all loaded from CDNs (internet connection needed)
- Deployed on Vercel

## Run locally

No build step or dependencies.

1. Clone the repo.
2. Open `index.html` in a browser, or serve the folder, for example:
   ```
   python -m http.server 8000
   ```
   then visit http://localhost:8000

## Project structure

```
index.html        page markup
css/              style.css, responsive.css
js/script.js      gallery popup + GSAP intro animation
img/              images and icons
```

## Known limitations / issues

- Landing page only; the features advertised are not built.
- Contact form does not submit anywhere.
- Page `<title>` is "ForGood" and some copy is leftover template text (e.g. "Uniting Hearts for Good", a "donation" form dropdown with values like food/clothes/footware, a placeholder email `foundation@code.com` as the mailto target).
- The gallery popup initially points to `img/gallery/1.jpg`, which does not exist in the repo.
- There is a stray malformed `</di v>` tag in `index.html`.
- Some gallery images are large (over 1 MB): `img/miss/33.jpg`, `img/miss/55.jpg`, `img/miss/77.jpg`.
- Contact details in the footer are partially masked placeholders.
