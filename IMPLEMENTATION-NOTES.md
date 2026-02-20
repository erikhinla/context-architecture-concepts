# Context Architecture — Wix Implementation Notes

## Overview
This page replaces `/digital-organizing/` on ocdexperience.com.
New URL: `/context-architecture/` (set up 301 redirect from old URL).

## Reference File
- **v4-client-ready.html** — Final approved design with all copy, layout, and interactions.
- Open it in a browser to see exactly how it should look and behave.

## Page Structure (top to bottom)

| Section | Wix Element | Notes |
|---|---|---|
| **Header/Nav** | Use existing site header | Add "Context Architecture" as active nav item, replacing "Digital O.C.D." |
| **Breadcrumb** | Text element | Home › Services › Context Architecture |
| **Hero** | 2-column strip | Left: text + 2 CTAs. Right: image placeholder (client to provide). |
| **Service Cards** | 4-column repeater or grid | 4 cards with emoji icons, titles, descriptions. Hover: teal border + slight lift. |
| **Stat Section** | Centered text strip | Large "130" number (teal, 20% opacity), headline, body text. |
| **3 Tiers** | 3-column pricing grid | Middle card ("Momentum") has teal border highlight. Each has bullet list + CTA button. |
| **Diagnostic Quiz** | Custom HTML embed or Wix interactions | 8 checkbox items. When 3+ checked, result box appears with CTA. See JS below. |
| **Process Steps** | 4-column grid | Numbers (01-04), titles, descriptions. |
| **Booking CTA** | Centered card | Price, description, single CTA button → link to booking/scheduling tool. |
| **Footer** | Use existing site footer | Add "Context Architecture" link under Services. |

## Design Specs

### Colors (CSS variables)
```
Background dark:    #141414
Background section: #1a1a1a
Card background:    #222222
Teal accent:        #5EC4AC
Text white:         #ffffff
Text light:         rgba(255,255,255,0.85)
Text muted:         rgba(255,255,255,0.5)
```

### Fonts
- **Inter** (headings + body) — already available via Google Fonts
- Fallback: Roboto, system sans-serif

### Spacing
- Section padding: 80px vertical
- Max content width: 1200px
- Card border-radius: 8px
- Card padding: 32px 24px

## Interactive Elements

### Diagnostic Quiz (JavaScript)
The quiz uses simple checkbox toggles. When 3+ items are checked, a result panel appears.

```javascript
function updateQuiz() {
    var n = document.querySelectorAll('.quiz-item.checked').length;
    document.getElementById('quizResult').classList.toggle('show', n >= 3);
}
```

**Wix options:**
1. **Custom HTML embed** — paste the quiz section HTML+CSS+JS directly
2. **Wix Interactions** — build with checkboxes + show/hide on condition (3+ checked)
3. **Wix Velo** — if using dynamic elements, use $w() to toggle visibility

### All CTAs
Every button on the page links to `#book` (the booking section at the bottom).
Replace the `#` in the final booking button with the actual scheduling URL (Calendly, Acuity, Wix Bookings, etc.).

## Responsive Behavior
- **Desktop (>900px):** Full grid layouts (4-col services, 3-col tiers, 4-col process)
- **Tablet (600-900px):** 2-column grids, hide text nav items (keep CTA button)
- **Mobile (<600px):** Single column everything

## SEO / Redirects
- Set up **301 redirect**: `/digital-organizing/` → `/context-architecture/`
- Page title: `Context Architecture — OCD Experience`
- Meta description: "Context Architecture structures your digital life for clarity, momentum, and fulfillment. File systems, email, security, and device sync — built by OCD Experience."

## Hero Image
Client needs to provide. Suggested: split-screen before/after (cluttered desktop → clean organized workspace). Aspect ratio 4:3.

## Questions?
Contact Erik at BizBuilders AI — erik@bizbuilders.ai
