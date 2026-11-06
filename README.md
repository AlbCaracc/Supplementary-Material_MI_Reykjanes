# Supplementary Data – Synchrotron Micro-CT and Geochemical Dataset

This GitHub repository contains supplementary material associated with the manuscript:

**A common near-Moho crystal mush zone under Fagradalsfjall and Sundhnúksgígar**

Alberto Caracciolo, Enikő Bali, Simon Matthews, Heini Merrill, Sæmundur A. Halldórsson, Marko Prašek, Takeshi Hanyu, Kenji Shimizu, Qing Chang, Takayuki Ushikubo

## Repository contents

The repository provides interactive synchrotron micro-computed tomography (micro-CT) reconstructions of four crystals from the 2023–2024 Fagradalsfjall and Sundhnúksgígar eruptions, together with the geochemical dataset associated with the manuscript.

### 1. Synchrotron micro-CT reconstructions

Four crystals were imaged at the SYRMEP beamline (Elettra) at a voxel resolution of 0.9 µm and an X-ray energy of 28 keV. The reconstructions allow visualisation of crystal interiors, melt inclusions and enclosed bubbles.

Two interactive visualisation tools are available:

- **[2D slice viewer](https://albcaracc.github.io/syrmep-crystal-tomography/tomo_4panel_viewer.html):** Displays sequential cross-sections through the four crystals, with individual playback controls and 500 µm scale bars.
- **[3D viewer](https://albcaracc.github.io/syrmep-crystal-tomography/tomo_3d_viewer.html):** Allows interactive rotation and sectioning of individual crystals, with segmented crystal, melt and void phases distinguished by X-ray attenuation.

| Crystal | Sample | Mineral |
|---|---|---|
| 102 | Fagradalsfjall 2023 | Plagioclase |
| 128 | Sundhnúksgígar December 2023 | Olivine |
| 150 | Sundhnúksgígar February 2024 | Olivine |
| 166 | Sundhnúksgígar March–May 2024 | Olivine |

### 2. Geochemical dataset

The repository also contains the geochemical dataset supporting the manuscript, including analytical data used to investigate melt inclusion compositions and the magmatic processes operating beneath Fagradalsfjall and Sundhnúksgígar.

## Technical information

- **2D slice viewer:** Every third slice displayed at 800 px resolution, with grey levels adjusted using the 0.5–99.8 percentile range for each crystal.
- **3D viewer:** Reconstructions use 3.6 µm voxels (4.5 µm for Crystal 102, with melt segmented on a 2.7 µm grid).
- **Phase segmentation:** Based on differences in X-ray attenuation, distinguishing voids (enclosed cavities), melt (glass-like material) and the surrounding crystal.

### Rebuilding the viewers

The original TIFF stacks and the Python packages `numpy`, `scipy`, `Pillow` and `matplotlib` are required.

```bash
cd code

# TOMO_DATA_ROOT = folder containing Eruption_2023, Svartsengi_23D, ...
# TOMO_OUT_DIR   = output folder (default: current folder)

python make_tomo_4panel.py   # 2D slice viewer
python make_tomo_3d.py       # 3D viewer
```

