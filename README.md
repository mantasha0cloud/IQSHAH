# Iqshah — product catalogue site

A single static page (`index.html`) that lists your pieces and sends
every "Buy on Meesho" tap straight to that product's Meesho page. No
server, no database, no build step — just this folder hosted for free
on GitHub Pages.

## What's in this folder

```
iqsha-site/
├── index.html      ← the whole site (HTML + CSS + JS in one file)
├── README.md        ← this file
└── images/
    ├── logo.png            ← full logo lockup
    ├── logo-mark.png        ← small circular "Q" mark used in the header/favicon
    └── product-*.jpg        ← your product photos
```

---

## Part 1 — Edit your details (do this first)

Open `index.html` in any text editor (Notepad, VS Code, or even GitHub's
own editor in the browser — see Part 2). Near the bottom, inside the
`<script>` tag, you'll find two things to edit:

### A) Your contact details
```js
const CONTACT = {
  whatsappNumber: "918369766855",   // your number with country code, digits only
  whatsappMessage: "Hi Iqshah! I'd love to know more about your collection.",
  email: "hello.iqshah@gmail.com",
  phone: "+91 83697 66855",
  instagram: "https://instagram.com/iqshah_ethnic"
};
```
Replace each value with your real WhatsApp number, email, phone, and
Instagram URL.

### B) Your products
```js
const PRODUCTS = [
  {
    name: "Maroon Medallion Tunic",
    tag: "Tunic · Tassel Cuffs",
    image: "images/product-maroon-medallion-tunic.jpg",
    link: "https://meesho.com/"
  },
  ...
];
```
For **every** product, replace `link` with that exact product's Meesho
page URL (open the product on Meesho, copy the URL from the address
bar, paste it in). I've filled in all 10 products from your photos —
you only need to swap in the real Meesho links.

To **add a new product**: drop a new photo in the `images` folder,
then copy one `{ ... }` block and edit its `name`, `tag`, `image`, and
`link`. To **remove one**, delete its `{ ... }` block.

---

## Part 2 — Put it on GitHub (free hosting)

1. Go to [github.com](https://github.com) and sign up / log in.
2. Click the **+** icon (top right) → **New repository**.
   - Name it anything, e.g. `iqsha-site`.
   - Set it to **Public**.
   - Don't add a README (you already have one) — just click **Create repository**.
3. On the new repo's page, click **uploading an existing file**.
4. Drag in everything from this `iqsha-site` folder — `index.html`,
   `README.md`, and the whole `images` folder — then click **Commit changes**.
   - Tip: if the site doesn't work later, it's usually because the
     `images` folder didn't upload correctly — check that
     `images/product-....jpg` files show up in the repo.
5. Go to the repo's **Settings** tab → **Pages** (left sidebar).
6. Under **Build and deployment → Source**, choose **Deploy from a branch**.
7. Under **Branch**, choose `main` and folder `/ (root)`, then **Save**.
8. Wait about a minute, then refresh the same Pages settings page — a
   green box will show your live URL, something like:
   ```
   https://your-username.github.io/iqsha-site/
   ```
   That's your permanent link.

### Making future edits
Whenever you want to change a Meesho link, add a product, or update your
number: open the file on GitHub (click on `index.html` → pencil/edit
icon), make the change, and click **Commit changes**. The live site
updates automatically within a minute — no re-uploading needed.

---

## Part 3 — Add the link to your Instagram bio

1. Open Instagram → your profile → **Edit profile**.
2. Tap the **Website** field.
3. Paste your GitHub Pages link (from Part 2, step 8).
4. Tap **Done**, then **Save**.

Your bio now shows a tappable link. Anyone who taps it lands on your
catalogue page; tapping any product's "Buy on Meesho" button sends them
straight to that product on Meesho.

**Optional:** if you use Instagram's "Link sticker" on Stories, you can
use the same URL there too.

---

## Notes

- All prices and stock stay on Meesho — this page is just a shopfront,
  so you never have to update prices in two places.
- The page is fully responsive (looks right on phones, which is where
  most of your Instagram traffic will come from).
- Everything is static, so there's nothing to "break" — worst case, you
  can always re-upload a fresh copy of this folder.
