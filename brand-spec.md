# Brand Spec — Márk Szabó Portfolio Landing Page

Cinematic dark UI for an AAA Environment & Hard Surface 3D Artist. Near-black stage, white hierarchy, one red accent, hairline borders, generous whitespace. Game-studio presentation quality (Naughty Dog / DICE / CD Projekt RED reference), not a generic template portfolio.

One-line summary: A black cinematic stage where white display typography, a single red accent, and a portrait that dissolves into a rainy city scene communicate AAA craft and quiet confidence.

## Tokens (OKLch)

| Token | Value | Source / role |
|---|---|---|
| `--bg` | `oklch(0.146 0 0)` | `#0B0B0B` — page background |
| `--surface` | `oklch(0.175 0 0)` | one step above bg; hover fills |
| `--fg` | `oklch(0.95 0 0)` | white type |
| `--muted` | `oklch(0.66 0 0)` | secondary text, icons |
| `--border` | `oklch(0.26 0 0)` | subtle 1px hairlines |
| `--accent` | `oklch(0.565 0.208 27)` | `#D62828` — used max twice per screen |

## Type stacks

- Display: `"Space Grotesk", "Segoe UI", Arial, sans-serif` — geometric, slight technical character; supports Latin Extended (Á, Ó).
- Body: `"Inter", "Segoe UI", Arial, sans-serif`
- Signature: `"Caveat", "Segoe Script", cursive` — handwritten sign-off only.

## Visual language rules

1. Near-black stage with white information hierarchy; the red accent is reserved for a kicker and one secondary moment per screen — never decorative scatter.
2. Hairline borders (1px) only. No cards, no rounded bubbles, no glassmorphism, no bright gradients.
3. Kickers are small tracked caps; display headings use tight negative tracking. Generous whitespace between every block.
4. Cinematic bleed: the portrait and the rainy-city environment fade into the page through soft radial masks — nothing sits inside a frame.
5. Minimal line icons (1.5px stroke) for social and stats; no colorful icon cards.
