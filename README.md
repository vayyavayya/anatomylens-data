# anatomylens-data

Model data for **AnatomyLens** (3D anatomy and CT-slice teaching atlas). It is served to the app through jsDelivr:
`https://cdn.jsdelivr.net/gh/vayyavayya/anatomylens-data@<tag>/v2/<file>`.

This is a teaching model, not patient anatomy.

## Attribution (required — CC BY-SA)

- **3D geometry, names, hierarchy, label leader lines (landmarks), muscle attachments:** [Z-Anatomy](https://github.com/Z-Anatomy/Models-of-human-anatomy) (`Startup.blend` in `Z-Anatomy.zip`), **CC BY-SA 4.0**. It is derived from **BodyParts3D**, © The Database Center for Life Science (DBCLS), licensed **CC BY-SA 2.1 Japan**.
- **Definitions (`defs.json`):** Wikipedia text carried in Z-Anatomy, **CC BY-SA**.
- **Latin terms:** the Terminologia Anatomica 2 table (`TA2.csv`) in the same Z-Anatomy repository.

## What was changed

These files are adapted material. They are licensed **CC BY-SA 4.0** under the same terms.

| File | What it is | How it was made |
|---|---|---|
| `v2/<system>.bin` | gzip; uint16-quantised xyz, then per-object uint16/uint32 index arrays | Exported from Startup.blend (modifiers evaluated), decimated with fast-simplification |
| `v2/index.json` | objects, landmarks, muscle attachments, colours | from the Z-Anatomy object tree and label leader lines (729 landmarks kept; left side mirrored from right where the left leaders were broken) |
| `v2/adjacency.json` | neighbours ≤ 3 mm, nerves/vessels ≤ 2 mm or inside, landmarks ≤ 5 mm | computed from the meshes (exact triangle distance, BVH) |
| `v2/annotations.json` | per-structure markings + short AI note | Claude **ranks** geometry-derived candidate IDs and writes a 2–3 sentence note. Every ID is validated against `index.json`. AI-generated; not reviewed by a physician unless marked. |
| `v2/landmarks-derived.json` | skull-base points derived from geometry | method recorded per point |

Axes: Blender Z-up, metres. +x = patient left, −y = anterior, +z = superior.
