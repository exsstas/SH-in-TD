# Spherical Harmonics Lighting Toolkit for TouchDesigner

A real-time diffuse lighting system for TouchDesigner based on L2 spherical harmonics.
Stores incoming light as 27 numbers per probe in a 3D world-space grid.
The same field can drive geometry shading, particle behaviors, and any other system in the scene.

**Requires TouchDesigner 2025.31550 (with POPs) or newer.**

---

## Videos

| | Title |
|---|-------|
| SH01 | [Storing Light as Data](https://youtu.be/oLuqwNLJXvQ) — theory |
| SH02 | [Lighting Toolkit for TouchDesigner](https://youtu.be/q3ZLM3AYzUU) — toolkit walkthrough |
| SH03 | [Building the Project from Scratch](https://youtu.be/eFERLrsXv3c) — full project build, one take |

---

## Files

| File | Description |
|------|-------------|
| `project_file_from_tutorial.toe` | Main project file — includes all examples from SH02 and the full scene from SH03 |
| `Calculator_EnvMap.tox` | Encodes a static or animated HDR environment map into the probe grid |
| `Calculator_spherical_lights.tox` | Point and spherical area lights with inverse-square falloff |
| `Calculator_line_lights.tox` | Continuous line-strip emitters (works with Text POP in line mode) |
| `Generator_3atmo.tox` | Three orbiting virtual suns — procedural animated light field |
| `Generator_simple.tox` | Minimal procedural generator — starting point for custom shader work |
| `Modifiers.tox` | Band filter, sigma windowing, rotation, HSV, blend tools |
| `SH_Analyze_Basic_L1.tox` | Extracts dominant light direction per RGB channel from the field |
| `3DTex_encode.tox` | Converts probe POP attributes into nine RGBA 3D textures for GPU sampling |
| `SH_Only_MAT.tox` | Phong, normal-mapped Phong, and PBR materials with SH diffuse |
| `SH in TD Developer_Reference_06-2026.pdf` | Full shader reference — intended for use with an AI coding assistant |

---

## Limitations

- Diffuse lighting only — no specular, glossy reflections, or metallic response
- No occlusion between light sources and probes
- Ringing from very sharp sources — use sigma windowing in Modifiers.tox to reduce it

---

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use and modify for any purpose, attribution required.

---

## Info

[Support project on Patreon](https://patreon.com/exsstas)

[Personal site and contacts](https://www.exsstas.art/)
