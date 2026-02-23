#  Generative Adversarial Networks (GANs): Research-Oriented Implementations

##  Overview

This repository contains research-focused and reproducible implementations of
Generative Adversarial Networks (GANs). The project emphasises theoretical
correctness, training stability, and empirical evaluation.

It is designed to serve both as:
- A research and learning reference for GAN fundamentals and variants
- A resume-ready demonstration of deep learning and generative modelling skills

---

##  Research Motivation

Although GANs are powerful generative models, they are difficult to train due to:
- Minimax optimisation instability
- Mode collapse
- Vanishing or exploding gradients

This repository explores how architectural changes and loss-function
Reformulations improve convergence and sample quality, with a strong focus on
Wasserstein-based GANs.

---

##  Models Implemented

- Vanilla GAN (Baseline adversarial training)
- DCGAN (Convolutional GAN for image data)
- Wasserstein GAN (WGAN)
- Wasserstein GAN with Gradient Penalty (WGAN-GP)
- Style GAN
- Pass GAN
- Cycle GAN

Each model is implemented using explicit training loops to avoid black-box
abstractions and improve conceptual clarity.

---

##  Mathematical Formulation

### Vanilla GAN Objective

min_G max_D E[x ~ pdata][log D(x)] + E[z ~ pz][log(1 - D(G(z)))]

### Wasserstein GAN Objective

min_G max_D E[x ~ pdata][D(x)] - E[z ~ pz][D(G(z))]

### Gradient Penalty (WGAN-GP)

λ E[(||∇x̂ D(x̂)||₂ − 1)²]

---

##  Experimental Design

- Controlled experiments across identical datasets
- Comparison of loss convergence behavior
- Visualization-based qualitative evaluation
- Manual hyperparameter tuning


---
