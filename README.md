# Synchrotron micro-CT of four crystals

Micro-CT of four crystals from the 2023-2024 Fagradalsfjall and Svartsengi eruptions, imaged at the SYRMEP beamline (Elettra).

- **[Slice viewer](https://albcaracc.github.io/syrmep-crystal-tomography/tomo_4panel_viewer.html)**: the four crystals each with its own play button and 500 µm scale bar.
- **[3D viewer](https://albcaracc.github.io/syrmep-crystal-tomography/tomo_3d_viewer.html)**: rotate and cut through each crystal; choose the crystal from the drop-down.

| Panel | Crystal | Sample | Mineral |
|---|---|---|---|
| 1 | 102 | Fagradalsfjall 2023 | Plagioclase |
| 2 | 128 | Svartsengi December 2023 | Olivine |
| 3 | 150 | Svartsengi February 2024 | Olivine |
| 4 | 166 | Svartsengi March-May 2024 | Olivine |

## Data

- Voxel size 0.9 µm, 28 keV.
- Slice viewer: every 3rd slice, 800 px frames. Grey levels are auto-contrasted per crystal (0.5-99.8 percentile of the stack).
- 3D viewer: 3.6 µm voxels (4.5 µm for Crystal 102; its melt is segmented on a 2.7 µm grid).

## Phases in the 3D viewer

Phases are set from grey level (X-ray attenuation):

- **Voids**: enclosed cavities.
- **Melt**: glass-like material.
- **Crystal**: everything else. Zoning shows as shading.

## Rebuild

Needs the original TIFF stacks plus `numpy`, `scipy`, `Pillow` and `matplotlib`.

```bash
cd code
# TOMO_DATA_ROOT = folder containing Eruption_2023, Svartsengi_23D, ...
# TOMO_OUT_DIR   = output folder (default: current folder)
python make_tomo_4panel.py   # slice viewer
python make_tomo_3d.py       # 3D viewer
```
