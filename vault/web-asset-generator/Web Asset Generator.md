# Web Asset Generator

Invoke: `/web-asset-generator`
Source: [alonw0/web-asset-generator](https://github.com/alonw0/web-asset-generator)

---

## What It Does

Generates production-ready web assets from a logo image, emoji, or text slogan:
- Favicons (16x16, 32x32, 96x96, favicon.ico)
- PWA app icons (180x180, 192x192, 512x512)
- Open Graph / social media images (Facebook, Twitter, WhatsApp, LinkedIn)
- Automatic `manifest.json`
- HTML meta tags ready to paste

---

## Requirements

- Python 3.6+
- Pillow: `pip install Pillow`
- pilmoji (for emoji-based icons): `pip install pilmoji`

---

## Workflow

The skill uses `AskUserQuestion` for every choice to show clickable UI options instead of typing. Use this as the standard flow:

### Step 1: Asset type
Select: Favicons only, App icons only, Social images only, or Everything.

### Step 2: Source material
Select: Logo image, Emoji, Text/slogan, or Logo + text.

### Step 3: Run the script

**From a logo image:**
```bash
python scripts/generate_favicons.py <source_image> <output_dir> all
python scripts/generate_og_images.py <output_dir> --image <source_image>
```

**From an emoji:**
```bash
# Get suggestions based on a description
python scripts/generate_favicons.py --suggest "coffee shop" output/ all

# Generate with the chosen emoji
python scripts/generate_favicons.py --emoji "☕" output/ all
python scripts/generate_favicons.py --emoji "☕" --emoji-bg "#F5DEB3" output/ all
```

**From text:**
```bash
python scripts/generate_og_images.py output/ \
  --text "Your Tagline Here" \
  --logo /path/to/logo.png \
  --bg-color "#4F46E5"
```

### Step 4: Move files to outputs
```bash
cp output/* /mnt/user-data/outputs/
```

### Step 5: Provide HTML tags

**Favicons:**
```html
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="icon" type="image/png" sizes="96x96" href="/favicon-96x96.png">
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="192x192" href="/android-chrome-192x192.png">
<link rel="icon" type="image/png" sizes="512x512" href="/android-chrome-512x512.png">
```

**Open Graph:**
```html
<meta property="og:image" content="/og-image.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:image:alt" content="Your description here">

<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:image" content="/twitter-image.png">
<meta name="twitter:image:alt" content="Your description here">
```

### Step 6: Code integration

The skill offers to inject the tags into your codebase automatically. It detects your framework:

| Framework | Target file |
|---|---|
| Next.js (App Router) | `app/layout.tsx` |
| Next.js (Pages Router) | `pages/_document.tsx` |
| Astro | `src/layouts/Layout.astro` |
| SvelteKit | `src/app.html` |
| Vue/Nuxt | `app.vue` or `nuxt.config.ts` |
| Gatsby | `gatsby-ssr.js` |
| Plain HTML | `index.html` |

### Step 7: Testing

After deployment (not localhost), test at:
- Facebook: https://developers.facebook.com/tools/debug/
- Twitter: https://cards-dev.twitter.com/validator
- LinkedIn: https://www.linkedin.com/post-inspector/
- Generic: https://www.opengraph.xyz/

---

## Image Specs

### Favicons and app icons
| File | Size | Use |
|---|---|---|
| favicon-16x16.png | 16x16 | Browser tab (small) |
| favicon-32x32.png | 32x32 | Browser tab (standard) |
| favicon-96x96.png | 96x96 | Shortcut icon |
| favicon.ico | Multi-res | Legacy fallback |
| apple-touch-icon.png | 180x180 | iOS home screen |
| android-chrome-192x192.png | 192x192 | Android home screen |
| android-chrome-512x512.png | 512x512 | Android splash screen |

### Social images
| File | Size | Use |
|---|---|---|
| og-image.png | 1200x630 | Facebook, WhatsApp, LinkedIn |
| twitter-image.png | 1200x675 | Twitter large card |
| og-square.png | 1200x1200 | Square variant |

---

## Platform size and format limits
| Platform | Max file size | Formats |
|---|---|---|
| Facebook, LinkedIn, WhatsApp | 8 MB | PNG, JPG |
| Twitter | 5 MB | PNG, JPG, WebP |

---

## Best Practices

**Source images:**
- Use the largest available version (scripts scale down)
- Square or near-square logos produce best favicon results
- PNG with transparent background works best for favicons
- Solid backgrounds are recommended for app icons and social images

**Text in social images:**
- Keep text under 60 characters for best font sizing
- Short text (under 20 chars): 144px font
- Medium text (21 to 40 chars): 120px font
- Long text (41 to 60 chars): 102px font
- Very long text (over 60 chars): 84px font

**Contrast:**
- Minimum 4.5:1 contrast ratio for WCAG AA compliance
- The `--validate` flag runs an automated contrast check

**Deployment:**
- OG images must be served via HTTPS (not localhost)
- Use absolute URLs in meta tags: `https://yourdomain.com/og-image.png`

---

## Validation

Both scripts support `--validate` to check dimensions, file size, format, and contrast before deployment. Always run validation before shipping to production.
