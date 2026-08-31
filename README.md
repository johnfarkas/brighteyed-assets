# Bright Eyed — Brand Assets

The asset library for **Bright Eyed**, an all-day café at 102 S. Weber, Colorado Springs.
Companion café to the CoSpark Center, and a daughter brand of the
[CoSpark design system](https://cospark.farkas.design/).

## What is here

| Page | Contents |
| --- | --- |
| `index.html` | Hub, and how the geometry works |
| `logo/` | Vertical and horizontal lockups, and the icon — SVG + PNG, full color and single ink |
| `color/` | The seven colors, hex values, roles, contrast pairs, supporting neutrals |
| `typography/` | Cormorant Garamond and Jost — downloads, embed code, type scale |

Raw files live in `assets/logo/`.

## The mark

A square quartered into four colors with the spark knocked out in paper. The spark is
CoSpark's own geometry, rotated 45° — tips up, down, left, right. One value governs
everything: **S**, the radius of the spark's points.

| Value | Role |
| --- | --- |
| `S` | Radius of the spark's points — governing |
| `T = 2S` | Tile side; points tangent to all four edge midpoints |
| `S ⁄ 3` | The spacing unit — governs both lockups and the page |
| `S ⁄ 2` | Clear space outside the tile, all four sides |

Quadrant order is a light/dark checker — coral top-left, dusk top-right, wine
bottom-left, garden bottom-right. Same-value quadrants sit diagonal, never adjacent.
Peach and apricot never take a quadrant. The tile rotates 0/90/180/270 and nothing else.

Scale floors: the four-color tile holds to **40 px**; single ink to **24 px**.

## Palette

| Name | Hex | Role |
| --- | --- | --- |
| Paper | `#FFF6EE` | Knockout · ground |
| Peach | `#FFDCC5` | Ground |
| Apricot | `#FFB07C` | Ground |
| Coral | `#E76F51` | Quadrant · ground |
| Garden | `#8FAE8B` | Quadrant · ground |
| Dusk | `#33344A` | Quadrant · ink |
| Wine | `#3A0A1C` | Quadrant · ink |

Coral is a ground, never an ink. Wine is the safe default ink — it reads on every color
in the palette. Wine and dusk are accessories, not staples: the café is called Bright
Eyed, and the surfaces should say so.

## Typefaces

**Cormorant Garamond** SemiBold 600 for display and the wordmark.
**Jost** 300/400/500/600 for every working word. Both SIL OFL.

## Notes on the files

The SVG lockups carry the wordmark as live text in Cormorant Garamond SemiBold — install
the font or use the PNG. Outlined SVG and vector EPS for print vendors are in production.
The single-ink versions knock the spark out to transparent, so the ground shows through.

## Local preview

```
python3 -m http.server 8000
```

Then open <http://localhost:8000/>.

## Publishing

Files sit at the repository root, so GitHub Pages serves them with no build step:
Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`.
The `CNAME` file points the site at **brighteyed.farkas.design** — add a DNS record for
that subdomain pointing to GitHub Pages and it will resolve.
