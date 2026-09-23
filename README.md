# Umerang Lab — event tracking test site

A one-page test site for the Umerang **Metrics & Events Catalog**. Using the page sends real events to the Umerang collector on **staging** (merchant `UTA7F4D868`), so each catalog event can be checked in the dashboard.

## What it covers

- All 62 browser-side events in the catalog: core events (session, page view, navigation, scroll, clicks, forms, search, video, downloads, outside links, popups, element views, print), products, cart, checkout and order, subscriptions, customer identity, and custom events.
- The 7 server-side events are listed on the page but never sent from the browser.

## How events are sent

- **Section 1 (core) events** come from the collector's own auto-capture, as the catalog describes. A switch near the top also sends them from the page, using the catalog's field names.
- **All other events** are sent by the page with `umerang.track()` and `umerang.identify()`, using the catalog's field names.

## Event log

The **Event log** button opens a panel with two tabs:

- **Log** decodes every batch the collector sends to `stage-api.clubeez.com` and shows its HTTP status.
- **Coverage** ticks each catalog event once it has been sent successfully.

Clicks on the panel itself are kept out of tracking.

## Files

- `index.html`: the whole site (HTML, CSS and JavaScript).
- `media/`: sample video ("Flower", CC0, from MDN) and product images.
- `files/`: sample PDF, CSV and ZIP used by the download events.

Test data only. The page asks search engines not to index it.
