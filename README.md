# Kandersteg 2027 Donation Tracker

A single-page donation tracker for the Lusk 153 Scout Group's fundraising for a camp to Kandersteg, Switzerland, in July 2027. The target is €15,000.

The site is one static file, `index.html`, with inline CSS and JS. The only external dependency is Google Fonts (Barlow, Barlow Condensed). It is intended to be hosted on GitHub Pages.

## What the page shows

- Progress bar and running total against the goal
- Scrolling ticker of the 10 latest donations
- Donor list with show more / show less
- "Ways to donate" section
- Sponsor cards
- Dark mode support

## Updating the data

There is no backend. Edit the data at the top of the `<script>` block in `index.html`, then commit and push.

| Constant | Contents |
| --- | --- |
| `CAMP` | `goal` (15000), `raised` (manual running total), `donateUrl` (leave empty until there is a link) |
| `DONATIONS` | Array of `{ name, amount, date }`. Use `"Anonymous"` to hide a donor's name. |
| `SPONSORS` | Array of `{ name, tag, details[], contact }` |

While `donateUrl` is empty, the donate button shows "Link coming soon".

## Hosting

Enable GitHub Pages under Settings → Pages, using the `main` branch.

## Open items

- Online donation link (`donateUrl`), if we use a platform such as JustGiving or GoFundMe. Switching platforms would change how the ticker gets its data.
- Bank transfer details (reference: "Kandersteg")
- Confirm the cash/card-to-a-leader wording
- Keep the raised total and donations up to date
- Add further sponsors and one-off donors

## Privacy

Donor names are shown by default. Donors can choose to appear as "Anonymous".
