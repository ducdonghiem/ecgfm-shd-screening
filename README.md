# echofm-shd-transfer

Official repository for the paper:

**Domain-Adapted Fine-Tuning of ECG Foundation Models for Multi-Label Structural Heart Disease Screening**

## Overview

This repository contains the code and materials for our study on multi-label structural heart disease (SHD) screening from 12-lead ECGs using the EchoNext Mini-Model benchmark.

We evaluate whether open ECG foundation models can improve detection of six echo-confirmed moderate-or-greater SHD phenotypes, including:

- reduced left ventricular ejection fraction (LVEF ≤ 45%)
- increased left ventricular wall thickness (LVWT ≥ 1.3 cm)
- aortic stenosis
- mitral regurgitation
- tricuspid regurgitation
- right ventricular systolic dysfunction

The study compares multiple modeling strategies, including engineered-feature baselines, waveform models trained from scratch, frozen foundation-model embeddings, and domain-adapted partial fine-tuning of ECG-FM. Additional experiments examine late fusion with tabular covariates, LoRA, alternative ECG foundation models, mixture-of-foundation-model strategies, binary-vs-multi-label training, and downsampling.

## Status

This repository is being prepared alongside the camera-ready version of the paper and will be updated gradually until the conference.

Planned updates include:

- training and evaluation code
- model configuration files
- figure-generation scripts
- result summaries and appendix assets
- documentation for reproducing the main experiments

## Note

The repository is currently under active cleanup and organization. Some files, scripts, and instructions may be incomplete during this period. Please check back for incremental updates.

## Citation

A citation entry will be added after the final camera-ready version is completed.

## Contact

For questions related to the paper or repository, please contact the corresponding author listed in the paper.