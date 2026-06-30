# Front-End
Simple Front-End Project

# 🎨 Studio Agency — Landing Page

A responsive, single-page landing site for a creative/design agency, built with **HTML5** and **Bootstrap 5**. Includes a hero section, services, portfolio, company timeline, team, client logos, and a contact form.

---

## 📌 Sections

| Section | Description |
|---------|-------------|
| **Navbar** | Fixed-top, scroll-aware navigation with smooth-scroll links to all sections |
| **Landing / Hero** | Full-screen intro with heading and call-to-action button |
| **Services** | Three feature cards (E-Commerce, Responsive Design, Web Security) with icon badges |
| **Portfolio** | 6-item image grid with hover overlay effect |
| **About** | Vertical timeline of company milestones (2009–2020) with alternating left/right layout |
| **Team** | Team member cards with photo, role, and social links |
| **Client Logos** | Row of partner/client brand logos |
| **Contact** | Contact form (name, email, phone, message) on a map-background section |
| **Footer** | Copyright, social icons, and legal links |

---

## 🛠️ Tech Stack

- **HTML5**
- **Bootstrap 5.3.2** (local copy in `bootstrap/`)
- **Font Awesome** (local + CDN fallback)
- **Bootstrap Icons** (CDN)
- **Google Fonts** — Montserrat & Bebas Neue
- Custom `style.css` and `script.js`

---

## 📁 Expected File Structure

```
project/
  index.html
  style.css
  script.js
  bootstrap/
    bootstrap-5.3.2-dist/
      css/bootstrap.min.css
      js/bootstrap.bundle.min.js
    fontawesome/
      fontawesome/css/all.min.css
  imgs/
    navbar-logo.svg
    1.jpg ... 6.jpg          (portfolio images)
    1(1).jpg ... 4(1).jpg    (about/timeline images)
    1(2).jpg ... 3(2).jpg    (team photos)
    microsoft.svg, google.svg, facebook.svg, ibm.svg
    dotted-world-map-illustration-perspective-view-dark-isolated-background_226544-915.avif
```

All asset paths in `index.html` are relative, so this structure must be preserved for the page to render correctly.

---

## 🚀 How to Run

No build step required — it's a static page.

1. Make sure `style.css`, `script.js`, the `bootstrap/` folder, and the `imgs/` folder are present alongside `index.html`
2. Open `index.html` directly in a browser, or serve it locally:
   ```bash
   npx serve .
   ```

---

## ⚠️ Known Issues / Things to Fix Before Publishing

- **Placeholder content**: All body text is still Lorem ipsum, and the `<title>` tag just says "Document" — update these before going live
- **Broken/dead links**: Social icons, nav CTA, and footer links all point to `#`
- **`<script src="script.JS">`** — the filename casing (`.JS`) won't match `script.js` on case-sensitive filesystems (Linux servers, GitHub Pages). Rename to lowercase `.js` to avoid a 404 in production
- **Duplicate Font Awesome**: loaded both locally (`bootstrap/fontawesome/...`) and via CDN — pick one to avoid redundant requests, and remove the placeholder `integrity="sha512-..."` hash on the CDN link (it's not a real hash, so the browser may block the stylesheet)
- **Contact form has no backend/action**: the `<form>` has no `action` or JS handler, so submissions currently do nothing
- **Large background image**: the `.avif` map background should be checked for file size/compression for production use

---

## 📋 Customization Notes

- Brand color (`#ffc800` / `bg-warning`) is used for icon badges and the submit button — update in `style.css` for a different palette
- Replace placeholder team names, roles, and images with real data
- Update footer copyright text and "Your Website" placeholder
