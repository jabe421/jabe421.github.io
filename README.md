# Armament International Catalog Demo V2

GitHub Pages-ready, data-driven catalog prototype.

- 6 demo products in each category: Handguns, Rifles, Shotguns, Suppressors, Optics, Accessories, Gear
- Gear includes Wrapped EDC Cobra Belt and EDC Fanny Pack
- Demo retail pricing
- Search, filters, sorting
- Browser-persistent Inquiry List
- No checkout/payment processing
- Product data: `assets/products.json`
- Product images: `assets/products/<category>/`
- Works when `index.html` is opened directly; the browser-file limitation is handled with a bundled fallback
- On GitHub Pages/web hosting, `products.json` is the live source of truth

See `PRODUCT-MANAGEMENT.md` for the product workflow.


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
