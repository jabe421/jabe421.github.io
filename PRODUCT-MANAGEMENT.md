# Armament International V2 — Product Management

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
  "img": "gear/example-product.webp",
  "tag": "NEW",
  "meta": "Short description",
  "sku": "AI-GR-007",
  "upc": "DEMO-AI-GR-007",
  "distributor": "",
  "distributorSku": "",
  "inventory": 0
}
```

## Important: opening index.html directly

Some browsers block JavaScript from reading a JSON file when an HTML file is opened directly as `file://.../index.html`. V2 now includes a bundled fallback so the supplied demo products still appear when you double-click `index.html`.

For ongoing catalog editing/testing, **GitHub Pages is the recommended environment** because `products.json` is loaded directly and remains the single source of truth.

The bundled fallback is automatically generated when this package is built; if you make product changes to `products.json` and continue testing only with `file://`, the fallback will not automatically update. On GitHub Pages it will use the current `products.json`.

Use JPG/JPEG/PNG/WebP product images. WebP is recommended.


## Standardized image paths

Use this structure for every product:

```text
assets/
├── products.json
└── products/
    ├── firearms/
    ├── suppressors/
    ├── optics/
    ├── accessories/
    └── gear/
```

For example, a Glock 19 image at:

`assets/products/firearms/g19g5.jpg`

must be referenced in `products.json` as:

```json
"img": "products/firearms/g19g5.jpg"
```

Do not put new product images directly in `assets/firearms/`, `assets/optics/`, etc. Those legacy directories have been consolidated into `assets/products/<category>/`.
