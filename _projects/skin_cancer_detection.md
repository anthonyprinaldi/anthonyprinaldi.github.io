---
title: "Skin Cancer Detection (Kaggle Competition)"
excerpt: "2D Medical Image Classification for Kaggle ISIC 2024 Competition"
collection: projects
---

This project involved training an 2D image classifier for skin cancer detection with (optional) meta-features for a [Kaggle Competition](https://www.kaggle.com/competitions/isic-2024-challenge/overview).

I fine-tuned the EfficientNet B1 model [[Tan & Le, 2020](https://arxiv.org/abs/1905.11946)] with a new classifier head to match the binary prediction of this task. I add a simple shallow network for passing meta-features to the network if the user desires, which will be concatenated with the EfficientNet output features before classification. I rely on `PyTorch` for modelling and `Lightning` for training. I fine-tuned the model locally using an `NVIDIA TITAN Xp` GPU.

**I obtained a public LB score of 0.137**. The score represents a fractional AUC with minimum score of 0 and maximum score of 0.2.

[Access my code here.](https://github.com/anthonyprinaldi/ISIC2024Kaggle){:target="\_blank" .btn}
