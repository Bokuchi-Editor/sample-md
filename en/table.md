# Table Layout Sample

This file demonstrates how the **Table Layout (Preview)** setting in Bokuchi changes the way tables are rendered.

> Setting location: **Settings → Advanced → Table Layout (Preview)**

Switch between the three modes while previewing this file to see the differences at a glance.

## What changes with each mode

| Mode | Column widths | Long content |
|------|---------------|--------------|
| Equal column widths | All the same | Wraps inside cells |
| Fit to content (wrap in cells) — default | Follow content | Wraps inside cells |
| Fit to content (horizontal scroll) | Follow content | Table scrolls horizontally |

---

## Example 1: One long column among short ones

This is where **Equal** and **Fit to content** differ most.
In **Equal** mode the short "ID", "Date", and "Status" columns get the same width as the long description, so the description column becomes a tall narrow strip that's hard to read.
In **Fit to content** mode the description column gets the room it needs and the short columns stay compact.

| ID | Date | Description | Status |
|----|------|-------------|--------|
| 001 | 2026-05-01 | Added a new user registration flow. Supports both OAuth2 sign-in (Google / GitHub / Microsoft) and email/password, and asks the user to fill in their profile on first login. | Done |
| 002 | 2026-05-03 | Switched the cache layer to Redis, dropping the average API response time from 280ms to 95ms. | Done |
| 003 | 2026-05-05 | Reworked pagination for the search API. Total-count retrieval is now lazy, which speeds up the first response. | In review |
| 004 | 2026-05-08 | Refreshed the notification settings UI: dark/light theme support and accessibility improvements. | In progress |

---

## Example 2: Many columns that don't fit on screen

This is where **horizontal scroll** mode shines.
In **Equal** and **Fit to content (wrap in cells)** modes every cell is squeezed so the whole table fits the pane. In **horizontal scroll** mode each column keeps its natural width and the table itself scrolls sideways.

| Order ID | Customer | Ordered At | SKU | Product | Qty | Unit price (USD) | Subtotal (USD) | Shipping address | Delivery | Owner |
|----------|----------|------------|-----|---------|-----|------------------|----------------|------------------|----------|-------|
| ORD-20260501-001 | Alice Carter | 2026-05-01 09:14 | SKU-A1023 | High-performance Laptop Pro 15 | 1 | 1,899 | 1,899 | 1234 Market St, San Francisco, CA 94103 | Delivered | Sato |
| ORD-20260502-007 | Brian Patel | 2026-05-02 13:22 | SKU-B2240 | Wireless Mechanical Keyboard | 2 | 149 | 298 | 88 Rue Saint-Antoine, 75004 Paris, France | In transit | Suzuki |
| ORD-20260503-014 | Chiara Romano | 2026-05-03 18:47 | SKU-C0098 | 32-inch 4K HDR Monitor | 1 | 699 | 699 | Via del Corso 120, 00186 Roma RM, Italy | Preparing | Tanaka |

---

## Example 3: A simple comparison table

When every cell is short there's no visible difference between the three modes. Everyday comparison tables read fine regardless of the setting.

| Feature | Plan A | Plan B | Plan C |
|---------|--------|--------|--------|
| Monthly | $9 | $19 | $39 |
| Storage | 10 GB | 100 GB | 1 TB |
| Support | Email | Email / Chat | 24h phone |

---

## How to try it

1. Open this file in Bokuchi and reveal the preview
2. Open **Settings → Advanced → Table Layout (Preview)**
3. Pick **Equal column widths** and watch Example 1's description column become a tall narrow strip
4. Switch back to **Fit to content (wrap in cells)** (the default) and notice the columns sizing themselves to the content
5. Switch to **Fit to content (horizontal scroll)** and confirm Example 2's table now scrolls horizontally instead of squeezing

> The HTML produced by the **Download** button (top-right of the preview) follows the same setting.
