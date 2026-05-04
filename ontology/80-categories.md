# The 80 canonical categories

The 80 categories are the **canonical instantiation** of the Meta-Globàlium — the consolidated ontological vocabulary the model proposes for human reality.

The 80 emerge from the 8 root categories (see [`8-root-categories.md`](8-root-categories.md)) by application of the **fourth radial axis** (PLA / Neutral / MON), generating layered expressions for each cardinal direction.

| Layer | Type | Count | Geometry |
|-------|------|-------|----------|
| Plasmatic | atemporal/foundational | 27 | inner sphere, radius 0–50 |
| Neutral | mediator/axial | 26 | mediator sphere, radius 60–80 |
| Mundane | temporal/phenomenal | 36 | outer sphere, radius 100–155 (cardinal vertices at 233) |
| **Total active** | | **89** | |

> The "80" is the canonical model number; the database has 89 active entries because cardinal polar vertices (single-letter labels at radius 233) are scaffolding for the 3D projection, not canonical categories. Filter `label NOT LIKE 'MON%[1-4]'` to obtain the canonical 80.

## Machine-readable export

Full data with multilingual labels, descriptions, and 3D coordinates: [`data/categories.json`](data/categories.json).

Schema summary (JSON):

```json
{
  "id": 10,
  "label": "AMO",
  "name_ca": "Amor",
  "name_en": "Love",
  "description_ca": "...",
  "description_en": "...",
  "type": "Neutral",
  "axis": null,
  "generation": 1,
  "coords_3d": {"x": 0, "y": 100, "z": 0}
}
```

Fields:
- `label` — canonical 3-letter code (stable identifier)
- `name_*` — human-readable name in language `*` (currently `ca`, `en`)
- `description_*` — full description (currently `ca`, `en`; HTML stripped, mojibake fixed)
- `type` — `Plasmàtica` / `Neutral` / `Mundana`
- `axis` — for axial categories: which dialectical axis they mediate
- `generation` — internal layering depth (0 = root, 0.5 = plasmatic expansion, 1 = first neutral, 1.5/1.75 = neutral expansions, 2 = mundane)
- `coords_3d` — projection coordinates for visualization

## Status: revisable

The specific 80-category instantiation derives from the European philosophical lineage (Llull → Xirinacs → Berenguer 2023–2026). It is **revisable** by design. The four reflective axes are stable; the specific labels and groupings of categories are open to refinement.

See [`../methodology/protocol-N2.md`](../methodology/protocol-N2.md) for the protocol governing revisions.

## See also

- [`4-axes.md`](4-axes.md) — the axes
- [`8-root-categories.md`](8-root-categories.md) — Cartesian skeleton
- [`fractal-N1-N2.md`](fractal-N1-N2.md) — how the 80 generate thousands of derived metacategories
- [`../lineage/xirinacs-1997.md`](../lineage/xirinacs-1997.md) — primary source
