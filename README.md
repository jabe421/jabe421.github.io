# F11 Arms Catalog Demo V3

GitHub Pages-ready, data-driven catalog prototype for **Factory 11 Firearms LLC**, branded as **F11 Arms**.

- Same V2 data-driven product structure
- 6 demo products in each category: Handguns, Rifles, Shotguns, Suppressors, Optics, Accessories, Gear
- Gear includes Wrapped EDC Cobra Belt and EDC Fanny Pack
- Demo retail pricing
- Search, filters, sorting
- Browser-persistent Inquiry List
- No checkout/payment processing
- Product data: `assets/products.json`
- Product images: `assets/products/<category>/`
- Brand assets: `assets/brand/`
- Works when `index.html` is opened directly via the bundled fallback
- On GitHub Pages/web hosting, `products.json` is the live source of truth

## Brand system

Primary brand: **F11 Arms**

Legal company name: **Factory 11 Firearms LLC**

Primary colors:
- Deep Graphite: `#0B0D0E`
- Panel Graphite: `#121618`
- Warm Brass: `#C79A3B`
- Highlight Brass: `#E1B65A`
- Bone White: `#F1EEE7`
- Muted Steel: `#667078`

Logo files:
- `assets/brand/f11-horizontal.svg` — primary website/header logo
- `assets/brand/f11-stacked.svg` — apparel/large-format stacked logo
- `assets/brand/f11-mark.svg` — icon/hat/fav icon mark
- `assets/brand/f11-mark-mono.svg` — one-color mark

## Standardized product image structure

All product images belong under:

`assets/products/<category>/`

Examples:
- `assets/products/firearms/g19g5.jpg`
- `assets/products/suppressors/example.jpg`
- `assets/products/optics/example.jpg`
- `assets/products/accessories/example.jpg`
- `assets/products/gear/example.jpg`

The matching `products.json` entry should use the same path relative to `assets`, for example:

`"img": "products/firearms/g19g5.jpg"`

Adding a product requires only:
1. Drop the image into the appropriate `assets/products/<category>/` folder.
2. Add one product object to `assets/products.json`.

No HTML or JavaScript changes are required when the site is hosted through GitHub Pages.
