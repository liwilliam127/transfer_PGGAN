# transfer_PGGAN
# Fine-Tuning PGGAN for High-Resolution Chest X-Ray Synthesis

This repository contains the code and models for fine-tuning a pretrained Progressive Growing GAN (PGGAN) to generate high-resolution chest X-ray (CXR) images adapted to the CheXpert dataset distribution.

We adopt a **partial fine-tuning strategy**, updating only the final ScaleBlock and toRGB layers of the generator, while keeping earlier layers frozen to preserve learned anatomical features.  
A **frozen DenseNet-121** pretrained on CheXpert serves as the discriminator backbone, with a lightweight binary classification head trained adversarially.  
Training is stabilized using the **Wasserstein GAN with Gradient Penalty (WGAN-GP)** objective.

This project aims to efficiently adapt synthetic CXR generation with minimal computational cost while maintaining clinical realism.

---

## Highlights
- **Partial generator fine-tuning** for efficient domain adaptation.
- **Frozen DenseNet-121** feature discriminator.
- **WGAN-GP** adversarial training for stability.
- **CheXpert** dataset for target domain adaptation.

---

## Acknowledgments
- Stanford ML Group for CheXpert.
- TorchXRayVision library.
- PGGAN pretrained models from Segal et al.

---

