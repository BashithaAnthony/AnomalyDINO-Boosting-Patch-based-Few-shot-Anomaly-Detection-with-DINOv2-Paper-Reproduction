# AnomalyDINO-Boosting-Patch-based-Few-shot-Anomaly-Detection-with-DINOv2-Paper-Reproduction

> ⚠️ **Status: Early / Work in Progress.** This project has just started. Setup and initial reproduction are in progress — no results yet. This README will be updated as work progresses.

Reproduction and extension of **[AnomalyDINO: Boosting Patch-based Few-shot Anomaly Detection with DINOv2](https://arxiv.org/abs/2405.14529)** (Damm et al., WACV 2025), done as part of an Image Processing & Machine Vision university module.

## About the paper

AnomalyDINO is a **training-free**, vision-only method for few-shot anomaly detection. It uses a frozen **DINOv2** backbone to extract patch-level features, builds a **memory bank** from a small number of normal reference images, and scores test images by nearest-neighbor distance in patch-feature space. This gives both:
- **Image-level anomaly detection** (is this image anomalous?)
- **Pixel-level anomaly segmentation** (where is the anomaly?)

Key contributions of the original paper: a tailored preprocessing pipeline (zero-shot foreground masking + augmentations for the few-shot setting) and a more robust score-aggregation statistic, evaluated on MVTec-AD and VisA.

Official code: [dammsi/AnomalyDINO](https://github.com/dammsi/AnomalyDINO)

## Goals of this project

1. **Reproduce** the core AnomalyDINO pipeline and validate results against the paper on a subset of MVTec-AD / VisA classes.
2. **Extend** the method with at least one modification (candidates below — to be narrowed down as work progresses).

## Status / Roadmap

- [ ] Set up environment and dependencies
- [ ] Download and organize MVTec-AD / VisA datasets
- [ ] Implement / adapt DINOv2 feature extraction
- [ ] Implement memory bank + nearest-neighbor scoring
- [ ] Reproduce baseline results on a subset of classes
- [ ] Decide on and implement extension/improvement
- [ ] Run ablations and write up results

## Planned repo structure

```
├── src/            # backbone, memory bank, preprocessing, scoring
├── configs/         # per-dataset / per-shot-count configs
├── scripts/         # data download, run experiments
├── notebooks/        # exploratory analysis
├── results/         # tables, plots
└── docs/            # notes on proposed improvements
```

*(Structure is provisional and will change as the project develops.)*

## Setup

_Coming soon — environment and installation instructions will be added once the pipeline is running._

## Team

- Bashitha Anthony
- Helitha Weerasinghe

## Citation

If referencing the original method, please cite:

```bibtex
@inproceedings{damm2024anomalydino,
  title={AnomalyDINO: Boosting Patch-based Few-shot Anomaly Detection with DINOv2},
  author={Simon Damm and Mike Laszkiewicz and Johannes Lederer and Asja Fischer},
  booktitle={Proceedings of the Winter Conference on Applications of Computer Vision (WACV 2025)},
  year={2025},
  url={https://arxiv.org/abs/2405.14529},
}
```

## License

This project builds on AnomalyDINO (Apache 2.0). See the [official repository](https://github.com/dammsi/AnomalyDINO) for details on the original license.
