# Technical Research and Decisions

## Frontend Framework Decision
### Decision: HTML + Tailwind CSS (No JavaScript)
### Rationale:
- Static website with no dynamic functionality required
- Tailwind CSS provides modern utility-first approach
- Zero JavaScript reduces complexity and improves performance
- Excellent browser compatibility
### Alternatives considered:
- React/Next.js (rejected: overengineered for static content)
- Plain CSS (rejected: Tailwind offers better maintainability)
- Bootstrap (rejected: Tailwind provides more modern design system)

## Image Optimization Strategy
### Decision: WebP format with JPG fallback
### Rationale:
- WebP offers superior compression while maintaining quality
- JPG fallback ensures compatibility with older browsers
- Responsive images using srcset for different viewport sizes
### Alternatives considered:
- PNG only (rejected: larger file sizes)
- AVIF (rejected: limited browser support)

## Layout Structure
### Decision: CSS Grid + Flexbox
### Rationale:
- Grid for overall page layout
- Flexbox for component-level arrangements
- Responsive without JavaScript
### Alternatives considered:
- Table-based layout (rejected: outdated)
- Float-based layout (rejected: more complex maintenance)

## Photo Gallery Implementation
### Decision: CSS Grid Gallery with Lightbox Alternative
### Rationale:
- Grid-based gallery with optimized image placement
- No JavaScript lightbox - opens full image in new tab
- Simple and effective for showcasing apartment photos
### Alternatives considered:
- JavaScript lightbox (rejected: adds unnecessary complexity)
- Carousel (rejected: requires JavaScript)

## Contact Method Implementation
### Decision: Static Contact Information + QR Code
### Rationale:
- Direct display of email and phone
- Static WhatsApp QR code image
- No form handling required
### Alternatives considered:
- Contact form (rejected: requires backend processing)
- Interactive messaging (rejected: requires JavaScript)

## Performance Optimization
### Decision: Built-in Browser Optimizations
### Rationale:
- Native lazy loading for images
- Preload critical assets
- Minimal CSS through Tailwind's purge feature
### Alternatives considered:
- JavaScript-based optimizations (rejected: unnecessary)