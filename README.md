# KLIK

One album for every photo from the day.

KLIK is a collaborative photo booth and memory platform. A host creates an event and shares a link or QR code. Guests join with a name and email (no account), shoot photo strips in the browser using hand gestures, and publish them to a shared album framed like postage stamps.

## Try it

Open `index.html` in Chrome. No build step.

- **Host:** Sign in, create an event, then share the invite link.
- **Guest (testing alone):** In the event's Share tab, choose "Open the link as a guest".
- **Booth:** Pinch and slide up/down to change filter, pinch and slide sideways to adjust strength, hold a peace sign ✌️ to start the timer. Both hands can be used at once.

## What's in the prototype

- Landing page, host sign-in, dashboard
- Create event: details, cover stamp, access (open or approval), upload window, Explore visibility
- Invite link, QR code, WhatsApp and email sharing
- Guest join, approval requests, returning guests recognised by email
- Hand-gesture booth (MediaPipe Gesture Recognizer) with live filters, strength control, 3s/5s timer, strip layouts, retake per shot
- Publish with per-photo visibility: Everyone at the event, or Only the host
- Host gallery (reorder, hide, delete, download), journal (drag photos and notes), guests, requests, settings
- Explore page for public albums

## Design

Figma is the source of truth for the design. See [FIGMA.md](FIGMA.md) for the file link, the workflow, and which frame maps to which screen.

## Current limits

- Data is stored in the browser (localStorage + IndexedDB). There is no server yet.
- Planned stack: Next.js + Supabase + Vercel.
- Arabic (RTL) version of the full site is not built yet. An earlier Arabic booth prototype is in `prototypes/`.
