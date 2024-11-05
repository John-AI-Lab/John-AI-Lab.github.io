---
title: Noisy Student

description: |
  A semi-supervised learning method which achieves 88.4% top-1 accuracy on ImageNet

layout: project
last-updated: 2019-11-11
---

**Noisy Student Training** is a semi-supervised learning approach that enhances model performance by combining self-training and knowledge distillation techniques. It involves the following steps:

1. **Teacher Model Training**: Train a teacher model using labeled data.
2. **Pseudo-Label Generation**: Use the teacher model to generate pseudo-labels for unlabeled data.
3. **Student Model Training**: Train a student model on a combined dataset of labeled and pseudo-labeled data, introducing noise during training to improve robustness.

This process can be iterated by treating the student as the new teacher to relabel the unlabeled data and training a new student model.

{:center: style="text-align: center"}
![image](/img/noisystudent/noisystudent.png){: width="40%"}
{:center}

## Key Components

- **Student Model Size**: The student model is designed to be equal to or larger than the teacher model, enabling it to learn effectively from the expanded dataset.
- **Noise Injection**: Noise is added to the student model during training to encourage learning from pseudo-labels. This includes:
  - **Input Noise**: Techniques like [RandAugment](https://paperswithcode.com/method/randaugment) for data augmentation.
  - **Model Noise**: Methods such as [dropout](https://paperswithcode.com/method/dropout) and [stochastic depth](https://paperswithcode.com/method/stochastic-depth) to regularize the model.

## Applications

Noisy Student Training has been successfully applied in various domains, including:

- **Image Classification**: Achieved state-of-the-art results on the ImageNet dataset.
- **Automatic Speech Recognition**: Improved performance in speech recognition tasks.
- **Facial Expression Recognition**: Enhanced accuracy in recognizing facial expressions from videos.

For more detailed information, refer to the original paper: [Self-training with Noisy Student improves ImageNet classification](https://arxiv.org/abs/1911.04252).
