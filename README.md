# AvantStay Guest Experience—Journey Map

Four guest-experience reports, cross-linked via the nav bar on each page:

- **`index.html`** — Vacation rentals. Six guest personas built from
  reservation and Zendesk data, their stage-by-stage journey, the current
  automated communication map, a brand-voice standard pulled from the GX
  Brand Voice Training Guide, and a four-quarter roadmap.
- **`hotels.html`** — Hotels. All ten AvantStay hotels, segmented by
  front-desk vs. no-front-desk/revenue-share operating model, in service of
  a specific goal (good reviews and revenue growth together) rather than
  revenue efficiency alone. Built from a Chef segmentation pull plus real
  TripAdvisor/Google/Booking.com/Expedia reputation data.
- **`comms-map.html`** — Comms map. A first-draft, message-by-message map
  of the real guest communication flow from booking confirmation through
  the post-stay review ask, built from real Booking Hub, Zendesk, Airbnb,
  and SMS examples with guest-identifying details replaced by placeholders.
- **`cx-routing.html`** — CX routing. The operating layer underneath the
  comms map: how a guest contact gets classified and routed, what the
  Duckie AI agent can and can't resolve on its own, the full guest email
  calendar, SpokePhone's role, and the recovery loop for an at-risk stay,
  plus a set of optimization/upsell ideas that connect this routing model
  back to the personas and reputation data on the other pages.

**Live site:** published via GitHub Pages once this repo's `main` branch has
a successful deploy—see the **Pages** section of repo Settings, or the
"deploy" run under the **Actions** tab, for the URL. Both pages deploy
together from the same branch.

## What this is

Static HTML, no build step, no framework, no dependencies—open either file
directly in a browser or edit it in place.

Numbers on both pages (reservation counts, dollar values, percentages,
ticket-to-value ratios) are **rounded for public sharing**. This repo is
public, so exact internal figures are intentionally not reproduced here;
see the internal source data for precise values.

## Editing

1. Edit `index.html` or `hotels.html` directly—content, copy, and the
   color/type variables at the top of each file's `<style>` block (`:root`)
   live in that one file. The two pages share the same design tokens but are
   otherwise independent; a change to one doesn't need to touch the other.
2. Commit and push to `main`.
3. GitHub Actions (`.github/workflows/deploy.yml`) rebuilds and republishes
   the Pages site automatically on every push—no manual deploy step.

## Brand

Colors and type are pulled from avantstay.com:

| Token | Value | Use |
| --- | --- | --- |
| `--ink` | `#022B54` | Brand navy—headings, hero/roadmap background |
| `--accent` | `#53C3D0` | Brand teal—accents on dark surfaces |
| `--link` | `#1C5D9F` | Link color |
| Body font | Source Sans 3 (Source Sans Pro family) | matches avantstay.com |
| Display font | Fraunces | open-license serif standing in for AvantStay's licensed display face |

The six persona identity colors are a separate categorical palette
(rust, slate blue, olive, teal, plum, rose) chosen for AA text contrast and
distinguishability under common forms of color vision deficiency, since the
brand's own palette (navy + teal) isn't wide enough to tell six personas
apart at a glance.

## Accessibility

- Skip-to-content link, landmark regions (`header`, `main`, `section`,
  `footer`), and a real heading hierarchy.
- Data tables use `<caption>`/`<thead>`/`scope="col"` and sit in a
  horizontally-scrollable, keyboard-focusable region for narrow viewports.
- Text contrast checked against WCAG AA for both brand and persona colors.
- Decorative color swatches (`.bar`, `.dot`) are `aria-hidden`; persona
  identity is always paired with visible text, never color alone.
- Visible focus rings (`:focus-visible`) and `prefers-reduced-motion` support.

## Publishing setup (one-time)

If Pages isn't already enabled: repo **Settings → Pages → Build and
deployment → Source: GitHub Actions**. After that, every push to `main`
deploys automatically via the included workflow.
