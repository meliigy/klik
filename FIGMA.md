# Figma ↔ code

**Source of truth: Figma.** Design changes are made in Figma first, then the code in this repo is updated to match.

Figma file: [Klik](https://www.figma.com/design/QWop4fDpniRYeC6xhK9Zh7/Klik?node-id=2001-24), page **Page 4**

## Workflow

1. Edit the screen in Figma.
2. Share the frame link (right-click the frame → Copy link to selection) and say what changed.
3. The frame is read from Figma and `index.html` is updated to match: layout, colors, type, copy.
4. The change is committed here with the frame link in the commit message.

Changes that apply everywhere (colors, fonts, spacing, buttons) should be made once, and the matching CSS variables in `index.html` (`:root`) get updated so every screen follows.

## Implemented from Figma

| Figma node | Screen | Notes |
|---|---|---|
| [2017:6706](https://www.figma.com/design/QWop4fDpniRYeC6xhK9Zh7/Klik?node-id=2017-6706) | New event, step 1 Details (v2) | Left = live paper card (blurred style photo behind, illustration, event name, date, description update as you type). Event Style = 9 swatches that change the background. Illustration is chosen in step 2. Title font La Machine Company is not loaded yet (Special Elite fallback). |

Assets exported from this frame are in `assets/new-event/`.

## Frame map (original code captures)

All frames are 1512 px wide desktop captures. They are currently named "Code - /" in Figma.

| Figma node | Screen | Route in `index.html` |
|---|---|---|
| 2015:571 | Landing page | `#/` |
| 2015:1434 | Landing page (copy) | `#/` |
| 2015:2247 | Sign in, empty | `#/signin` |
| 2015:2376 | Sign in, typing | `#/signin` |
| 2015:2505 | Sign in, filled | `#/signin` |
| 2015:2634 | New event, step 1 Details | `#/new` |
| 2015:2959 | New event, step 1 Details (variant) | `#/new` |
| 2015:3284 | New event, step 1 Details (variant) | `#/new` |
| 2015:3609 | New event, step 2 Access | `#/new` |
| 2015:3840 | New event, step 3 Review | `#/new` |
| 2015:4064 | Event, Share tab (after create) | `#/event/:id/share` |
| 2015:4315 | Event, Gallery empty | `#/event/:id/gallery` |
| 2015:4543 | Event, Journal empty | `#/event/:id/journal` |
| 2015:4763 | Event, Guests empty | `#/event/:id/guests` |
| 2015:4961 | Event, Requests (open access) | `#/event/:id/requests` |
| 2015:5158 | Event, Share tab | `#/event/:id/share` |
| 2015:5403 | Event, Settings | `#/event/:id/settings` |
| 2015:5748 | Booth, intro | `#/booth/:id` |
| 2015:6083 | Booth, intro (copy) | `#/booth/:id` |

## Not in Figma yet

These screens exist in code but have no frame yet: dashboard (`#/dashboard`), guest join and request sent (`#/join/:id`), guest album and My photos (`#/e/:id`), gallery and journal with photos, booth while shooting and review, publish dialog, explore (`#/explore`), mobile layouts, and the Arabic version.
