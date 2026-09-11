# AvantStay Guest Experience—Journey Map

A single-page guest-experience journey map and FY27 plan: six guest personas
built from reservation and Zendesk data, their stage-by-stage journey, the
current automated communication map, and a four-quarter roadmap.

**Live site:** published via GitHub Pages once this repo's `main` branch has
a successful deploy—see the **Pages** section of repo Settings, or the
"deploy" run under the **Actions** tab, for the URL.

## What this is

Static, single-file HTML (`index.html`). No build step, no framework,
no dependencies—open it directly in a browser or edit it in place.

Numbers on this page (reservation counts, dollar values, percentages,
ticket-to-value ratios) are **rounded for public sharing**. This repo is
public, so exact internal figures are intentionally not reproduced here;
see the internal source data for precise values.

## Editing

1. Edit `index.html` directly—content, copy, and the color/type variables
   at the top of the `<style>` block (`:root`) all live in one file.
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
