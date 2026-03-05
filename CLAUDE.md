# RRUGA STUDIOS — Shopify Theme

## Store Info
- **Brand:** RRUGA STUDIOS
- **Store URL:** saharasandtest.myshopify.com
- **Base Theme:** Horizon

## Brand Identity
- **Industry:** Fashion / Clothing
- **Aesthetic:** Minimal, Editorial, High-fashion
- **Design Inspiration:** ddd-Studio (clean, sparse, garment-focused)
- **Background Color:** #EBE5DD (warm off-white/sand)
- **Primary Text Color:** #000000 (Black)
- **Secondary Text Color:** #555555 (soft gray for details)
- **Button Background:** #1a1a1a (near black)
- **Button Text:** #FFFFFF (white)
- **Font:** Space Mono (provided as SpaceMono-Regular.woff2)
- **Font Fallback:** monospace

## Font Setup
- Font file: `assets/SpaceMono-Regular.woff2`
- Always use this CSS to load the font:
```css
@font-face {
  font-family: 'Space Mono';
  src: url('{{ 'SpaceMono-Regular.woff2' | asset_url }}') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

body, * {
  font-family: 'Space Mono', monospace;
}
```
- All text must use Space Mono — no exceptions
- Text should be UPPERCASE for headings, product names, labels
- Text should be lowercase for body copy and descriptions (as seen in reference)

## Color Palette
- **Page background:** #EBE5DD
- **All section backgrounds:** #EBE5DD (no white, no pure black sections except footer/CTA)
- **Text:** #000000
- **Borders/dividers:** #000000 or rgba(0,0,0,0.15) for subtle lines
- **Add to cart / Checkout button:** #1a1a1a background, #FFFFFF text

## Design Style
Inspired by ddd-Studio. Key principles:
- Extremely minimal — lots of whitespace, nothing unnecessary
- No rounded corners anywhere — everything is sharp/square
- No shadows, no gradients, no decorative elements
- Typography does the heavy lifting — all caps for labels and headings
- Products are the hero — large images, clean grid, no visual clutter
- Thin divider lines (1px) used to separate sections
- All text is small and sparse — never bold unless strictly necessary

## Header
- Minimal single-line header
- Left: navigation links (collection, info) — lowercase, small
- Center: brand name "RRUGA STUDIOS" — centered, uppercase
- Right: utility links (log in, currency, search, bag) — lowercase, small
- No background color — transparent over page background (#EBE5DD)
- No borders, no shadows
- Very minimal, flat layout

## Hero Section
- Full-width editorial image or video at top of homepage
- No text overlay on the image
- Image takes up roughly 40-50% of viewport height
- Clean cut — image ends, product grid begins immediately below

## Product Grid (Collection Page)
- 5 columns on desktop, 2 on mobile
- No card borders, no shadows, no rounded corners
- Product image takes full card width — tall portrait ratio
- Below image: product name in UPPERCASE Space Mono, very small font size
- Price below name, same small size
- No hover effects except subtle opacity change
- Background of grid: #EBE5DD — seamless with page
- Tight grid gap — products feel close together like a lookbook

## Product Page
- Split layout: left half = product image, right half = product details
- Left: large product image, full height, clean
- Right:
  - Product name in UPPERCASE, large
  - Product details in lowercase, centered, small text with dashes (- detail here)
  - "sizing chart +" expandable link
  - SIZE dropdown and QUANTITY (-/+) side by side at bottom
  - Price displayed clearly
  - "Add to cart" full-width dark button at very bottom
- Right panel has a visible border separating it from image
- Lots of whitespace — details are centered vertically in the right panel

## Cart / Bag
- Slide-in panel or full page
- Background: #EBE5DD
- Each item separated by a thin 1px divider line
- Product image on left (tall portrait), details on right
- Product name UPPERCASE, size below
- QUANTITY label with - / number / + controls
- Price aligned to the right
- TOTAL at bottom, large, UPPERCASE
- CHECKOUT button — full width, dark background, white UPPERCASE text
- X close button top right, minimal

## Footer
- Minimal, flat
- Dark background (#1a1a1a) or same page background
- Small uppercase links
- No decorative elements

## Typography Rules
- **Headings / Product names / Labels:** UPPERCASE, Space Mono
- **Body copy / Descriptions / Details:** lowercase, Space Mono
- **Font sizes:** Keep everything small and refined — never large blocks of text
- **Letter spacing:** Slightly wide (letter-spacing: 0.05em to 0.1em) for uppercase text

## Layout Rules
- No rounded corners anywhere (border-radius: 0 always)
- No box shadows
- No gradients
- 1px solid borders only where structurally needed
- Generous whitespace — padding and margins should be generous
- Max content width: 1400px centered
- Mobile: stack to single or 2-column layout

## File Structure
- `sections/` → theme sections (hero, header, footer, product cards etc.)
- `assets/` → CSS, JS, and font files (SpaceMono-Regular.woff2 goes here)
- `snippets/` → reusable components
- `templates/` → page templates
- `config/` → theme settings

## Important Rules
- Always keep designs **mobile responsive**
- Never break Shopify's built-in functionality — design only
- No animations except subtle opacity transitions (0.2s ease)
- Always use **Space Mono** font
- Always use **#EBE5DD** as background — never pure white
- When editing CSS, add to existing stylesheet — never duplicate rules
- Upload SpaceMono-Regular.woff2 to theme assets before starting

## Git Workflow
- Branch: `main` → connected to Shopify store via GitHub integration
- Every `git push` to `main` auto-deploys to the live store
- Always commit with a clear message describing what was changed
