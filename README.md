<div align="center">
  <h1>Domain-Adapted Fine-Tuning of ECG Foundation Models<br>for Multi-Label Structural Heart Disease Screening</h1>

  <p><strong>Duc N. Do<sup>1,2</sup>, Minh N. Do<sup>2</sup>, Dang Nguyen<sup>3</sup>, Khanh T.Q. Le<sup>1</sup>, Khoa D. Pham<sup>1</sup>, Hung N. Huynh<sup>1</sup>,</strong><br>
  <strong>Phi Pham-Van-Hoang<sup>1</sup>, Quan K. Huynh<sup>1</sup>, Ramez M. Odat<sup>4</sup>, Perisa Ashar<sup>5</sup>, Ethan Philip Lowder<sup>6</sup>,</strong><br>
  <strong>Minh H.N. Le<sup>1</sup>, Hoang Le<sup>1</sup>, Phat V.H. Nguyen<sup>1</sup>, Quan Le<sup>1</sup>, Jacques Kpodonu<sup>7</sup>, and Phat K. Huynh<sup>1,*</sup></strong></p>

  <p><small>
    <sup>1</sup>PASSIO Laboratory, North Carolina A&T State University, Greensboro, NC, USA<br>
    <sup>2</sup>Department of Computer Science, University of Manitoba, Winnipeg, MB, Canada<br>
    <sup>3</sup>Harvard T.H. Chan School of Public Health, Harvard University, Boston, MA, USA<br>
    <sup>4</sup>Department of Medicine, Jordan University of Science and Technology, Irbid, Jordan<br>
    <sup>5</sup>Department of Biomedical Engineering, Duke University, Durham, NC, USA<br>
    <sup>6</sup>Harvard Medical School, Boston, MA, USA<br>
    <sup>7</sup>Beth Israel Deaconess Medical Center, Harvard Medical School, Boston, MA, USA<br>
    <sup>*</sup>Correspondence: <a href="mailto:pkhuynh@ncat.edu">pkhuynh@ncat.edu</a>
  </small></p>

  <p><em>Accepted oral presentation at the 39th Canadian Conference on Artificial Intelligence (Canadian AI 2026).</em><br>
  <em>To appear in Proceedings of Machine Learning Research, vol. 318.</em></p>
</div>

> **Abstract:** *Transthoracic echocardiography is the reference standard for confirming structural heart disease (SHD), but its use as a first-line screening modality is limited by cost, workflow burden, and specialist availability. This study investigated whether open pretrained electrocardiogram (ECG) models can support echo-confirmed multi-label SHD detection using the public EchoNext Mini-Model benchmark. We focused on six moderate-or-greater echocardiography-derived abnormalities spanning reduced left ventricular ejection fraction, increased left ventricular wall thickness, aortic stenosis, mitral regurgitation, tricuspid regurgitation, and right ventricular systolic dysfunction. Under a common experimental pipeline, we compared engineered ECG features with gradient boosting, end-to-end waveform learning from scratch, and transfer from open ECG foundation models. We then evaluated continued in-domain self-supervised adaptation of ECG-FM on EchoNext waveforms followed by selective supervised fine-tuning, with emphasis on the trade-off between discrimination and adaptation cost. Among the evaluated configurations, the adapted ECG-FM models achieved the strongest overall performance. Across adaptation depths, peak macro-AUROC and macro-AUPRC reached 0.8509 and 0.4297, respectively, while a more parameter-efficient operating point preserved nearly identical AUROC (0.8501) and achieved the highest fixed-threshold macro-F1 (0.3691). Late fusion of the release-provided covariates did not improve threshold-independent discrimination, and the evaluated low-rank adaptation (LoRA) configuration, alternative foundation backbones, and mixture-of-foundation-model strategies did not surpass the best adapted single-backbone operating points. These findings indicate that, for ECG-based case finding and echocardiography triage, the most effective transfer strategy is to combine target-domain self-supervised adaptation with selective supervised updating of a pretrained ECG backbone.*

**Preprint available**: https://arxiv.org/abs/2604.23385

---

## Repository status

This repository is currently in progress. It supports the accepted Canadian AI paper and will be updated incrementally with code, experiments, and reproducible materials.

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

<!-- ## Status

This repository is being prepared alongside the camera-ready version of the paper and will be updated gradually until the conference.

Planned updates include:

- training and evaluation code
- model configuration files
- figure-generation scripts
- result summaries and appendix assets
- documentation for reproducing the main experiments

## Note

The repository is currently under active cleanup and organization. Some files, scripts, and instructions may be incomplete during this period. Please check back for incremental updates. -->

## Citation

If you use this work, please cite the following arXiv preprint:

```
@misc{do2026domainadaptedfinetuningecgfoundation,
  title={Domain-Adapted Fine-Tuning of ECG Foundation Models for Multi-Label Structural Heart Disease Screening},
  author={Duc N. Do and Minh N. Do and Dang Nguyen and Khanh T. Q. Le and Khoa D. Pham and Hung N. Huynh and Phi Pham-Van-Hoang and Quan K. Huynh and Ramez M. Odat and Perisa Ashar and Ethan Philip Lowder and Minh H. N. Le and Hoang Le and Phat V. H. Nguyen and Quan Le and Jacques Kpodonu and Phat K. Huynh},
  year={2026},
  eprint={2604.23385},
  archivePrefix={arXiv},
  primaryClass={cs.LG},
  url={https://arxiv.org/abs/2604.23385}
}
```

## Contact
For questions related to the paper, please contact the corresponding author listed in the manuscript.

For questions related to the code or repository, contact: **Duc Do** - dod2@myumanitoba.ca
