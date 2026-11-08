# Licences

| Dataset | Used for | Licence | Attribution |
|---|---|---|---|
| Z-Anatomy, Models of human anatomy (`Startup.blend`) — https://github.com/Z-Anatomy/Models-of-human-anatomy | meshes, names, hierarchy, label leader lines (landmarks), muscle attachments | CC BY-SA 4.0 — https://creativecommons.org/licenses/by-sa/4.0/ | "Z-Anatomy" by the Z-Anatomy project |
| BodyParts3D (via Z-Anatomy) | original 3D geometry | CC BY-SA 2.1 Japan — https://creativecommons.org/licenses/by-sa/2.1/jp/deed.en | © The Database Center for Life Science (DBCLS) |
| Wikipedia text (via Z-Anatomy) | `defs.json` definitions | CC BY-SA 4.0 | Wikipedia contributors |
| Terminologia Anatomica 2 table (`TA2.csv`, via Z-Anatomy) | Latin terms | as distributed in the Z-Anatomy repository | FIPAT / Z-Anatomy |
| This repository (adapted data: decimated meshes, adjacency, derived landmarks, annotations, synonyms) | the AnatomyLens app | CC BY-SA 4.0 (share-alike of the above) | AnatomyLens / Ajit Jose, adapted from Z-Anatomy & BodyParts3D |

`annotations.json` notes are AI-generated (Claude), ranked from geometry-derived candidates, not physician-reviewed unless marked.
`synonyms.json` entries each cite their own source (mostly Wikipedia, CC BY-SA 4.0); only the short term↔structure mapping is stored, no copied text.
