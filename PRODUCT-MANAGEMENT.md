# F11 Arms — Product Management

## Add a product

For the normal GitHub Pages/web-hosted version:

1. Drop the product photo into the appropriate folder:
   - `assets/products/firearms/`
   - `assets/products/suppressors/`
   - `assets/products/optics/`
   - `assets/products/accessories/`
   - `assets/products/gear/`

2. Add one object to `assets/products.json`.

No HTML or JavaScript editing is required when the site is hosted through GitHub Pages.

### Example

```json
{
  "id": "new-item",
  "name": "Example Product",
  "brand": "Manufacturer",
  "cat": "Gear",
  "price": 99,
  "img": "products/gear/example-product.webp",
  "tag": "NEW",
  "meta": "Short description",
  "sku": "F11-GR-043",
  "upc": "DEMO-F11-GR-043",
  "distributor": "",
  "distributorSku": "",
  "inventory": 0
}
```

## Important: opening index.html directly

Some browsers block JavaScript from reading a JSON file when an HTML file is opened directly as `file://.../index.html`. V3 includes a bundled fallback so the supplied demo products still appear when you double-click `index.html`.

For ongoing catalog editing/testing, **GitHub Pages is the recommended environment** because `products.json` is loaded directly and remains the single source of truth.

## Standardized image paths

```text
assets/
├── products.json
├── brand/
│   ├── f11-horizontal.svg
│   ├── f11-stacked.svg
│   ├── f11-mark.svg
│   └── f11-mark-mono.svg
└── products/
    ├── firearms/
    ├── suppressors/
    ├── optics/
    ├── accessories/
    └── gear/
```
