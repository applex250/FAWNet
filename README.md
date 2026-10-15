# FAWNet: Frequency-Aware Wavelet Network with Complementary Supervision for Remote Sensing Image Dehazing

This repository will host the official PyTorch implementation of

> **Frequency-Aware Wavelet Network with Complementary Supervision for Remote Sensing Image Dehazing**
> Yixin Wu, Jin Ning\*, Haipeng Li, Guo Zhang, Bin Duo
> Chengdu University of Technology
> *Submitted to IEEE Transactions on Geoscience and Remote Sensing (TGRS)*

## 🔒 Code Release

**Code will be released upon acceptance.**

This repository currently serves as the placeholder for the paper. The full
implementation — including the wavelet encoder blocks (WEB), the wavelet
frequency enhancement blocks (WFEB), the adaptive cross-scale decoder
refinement blocks (ACDRB) with boundary attention, the multi-scale output
head (MSH), and the training/evaluation pipeline for all seven datasets —
will be made publicly available here once the manuscript is accepted.

## Abstract

Remote sensing images acquired under hazy conditions suffer from contrast
degradation, color distortion, and detail loss. However, most existing
dehazing networks learn features without frequency awareness, and their
training objectives rarely exploit the complementary strengths of different
supervision signals. To address these issues, we propose a frequency-aware
wavelet network (FAWNet) that comprises a three-scale asymmetric wavelet
encoder–decoder backbone and a multi-granularity supervision framework. Each
wavelet encoder block embeds a differentiable Haar transform to separate
features into low-frequency and directional high-frequency parts, which are
then processed by dedicated frequency-aware pathways. The supervision
framework jointly constrains pixel fidelity, Fourier frequency alignment,
VGG-based perceptual similarity, and Sobel edge structure, together with
deep supervision on the intermediate predictions. Experiments on seven
remote sensing datasets covering both synthetic haze densities and
real-world scenes demonstrate that our FAWNet outperforms several
state-of-the-art dehazing methods with only 9.28M parameters, and our
empirical study shows that the Fourier frequency loss is the main
contributor to performance among the auxiliary supervision terms.

## Main Results (PSNR-Y (dB) / SSIM-Y)

| Dataset | SateHaze1K-thin | SateHaze1K-moderate | SateHaze1K-thick | RSID | RICE1 | RICE2 | CUHK-CR2 |
|---|---|---|---|---|---|---|---|
| FAWNet | 28.22 / 0.9789 | 31.53 / 0.9812 | 25.31 / 0.9498 | 28.71 / 0.9759 | 38.36 / 0.9918 | 38.10 / 0.9291 | 26.35 / 0.7549 |

*Model size: 9.28M parameters.*

## Citation

If you find this work useful, please cite:

```bibtex
@article{wu2026fawnet,
  title   = {Frequency-Aware Wavelet Network with Complementary Supervision
             for Remote Sensing Image Dehazing},
  author  = {Wu, Yixin and Ning, Jin and Li, Haipeng and Zhang, Guo and Duo, Bin},
  journal = {IEEE Transactions on Geoscience and Remote Sensing (submitted)},
  year    = {2026}
}
```

## Contact

- Corresponding author: Jin Ning ([ningjin@cdut.edu.cn](mailto:ningjin@cdut.edu.cn))
