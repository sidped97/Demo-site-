# Plumber Demo Website (with AI Chatbot)

A free, static demo website you can host on **GitHub Pages**. It includes:
- Mobile-friendly layout (HTML + CSS only)
- Smooth scrolling + colorful gradients
- Testimonials and services sections
- A **Contact** area with "Request a Free Quote" button
- **Chatbase AI Chatbot** embedded (bottom-right bubble)

## Folder Structure
```
plumber-demo-site/
├─ index.html
└─ assets/
   ├─ css/
   │  └─ styles.css
   └─ images/
      └─ (place your local images here if desired)
```

The site currently uses **Unsplash** placeholders (CDN) so you don't need to upload images to get started.
You can replace image `src` values in `index.html` with files you add under `assets/images/`.

---

## How to Put This Live on GitHub Pages (Step-by-Step)

1) **Create a GitHub account** (if you don't have one) at https://github.com

2) **Create a new repository**
   - Click **New** (top-left of your GitHub home)
   - Name it something like `plumber-demo-site`
   - Keep it **Public**, click **Create repository**

3) **Upload the files**
   - On your new repo page, click **Add file → Upload files**
   - Upload the three items from this folder:
     - `index.html`
     - `assets/` (the entire folder with its contents)
   - Click **Commit changes** at the bottom

4) **Enable GitHub Pages**
   - Go to **Settings** (tab at top of repo) → **Pages** (left sidebar)
   - Under **Build and deployment** set:
     - **Source:** *Deploy from a branch*
     - **Branch:** `main` (or `master`), **/ (root)**
   - Click **Save**
   - GitHub will display your live site URL, typically:
     `https://YOUR-USERNAME.github.io/plumber-demo-site/`

5) **Visit your site**
   - Open the URL shown in the Pages section
   - You should see the site live with the chatbot bubble in the bottom-right

---

## Updating the Chatbot (No Code Changes Needed)
- The chatbot loads from **Chatbase** using your bot's ID in the embed.
- When you change training data or settings in Chatbase, the website updates **automatically**.
- You do **not** need to re-deploy the site after changing Chatbase content.

### Where is the embed in code?
Open `index.html` and look for:
```html
<!-- Chatbase Chatbot Embed (provided by you) -->
<script>
  (function(){ /* ... */ })();
</script>
```
The `script.id` value is your Chatbase bot ID (`uuNckiKkpjKTcpYMCgM0z` in this demo).

> **Note:** Your "secret key" is only for server-side verification or advanced signed sessions. You do **not** need it for a basic website embed.

---

## Customization Tips
- Replace color variables in `assets/css/styles.css` (`:root{ ... }`) to match each client's brand.
- Swap image URLs in `index.html` to use local images under `assets/images`.
- Change the business name, phone, and email text in the **Contact** and **Hero** sections.
- Add more sections or pages if needed—GitHub Pages supports static sites easily.

---

## Troubleshooting
- **Site not loading?** Double-check GitHub Pages settings (branch = `main`, folder = `/root`).
- **Chat bubble not showing?** Ensure your embed script ID is correct and that Chatbase is active.
- **Images not appearing?** If you used local files, confirm paths (e.g., `assets/images/yourfile.jpg`).

Enjoy!
