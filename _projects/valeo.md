---
layout: page
title: Fine-Tuning of ResNet 50 for Defect Classification
description: Valeo AI challenge.
year: 2025
---

<figure style="margin: 2rem auto; width: 60%; text-align: center;">
  <img src="/images/valeo/confusion_matrix.png"
       style="width:100%; display:block;">
</figure>

This project was conducted during my 2nd year at Arts et Métiers. It is the first end-to-end deep learning project I carried out. It was a machine learning competition based on a dataset issued by Valeo. The goal was to perform defect classification on a dataset of pictures of microchips at the end of a production line. 

We were a hybrid team of data scientists and industrial engineers, all working together to build a functional solution working on real-world data and production context. 

This project is a classic computer vision with neural nets project, with a multi-class classification objective. The standard approach to tackle these is transfer learning. The backbone model is from the ResNet family or VGG. In this case, we chose ResNet 50 because it was well suited to our training infrastructure. Training was performed using Google Colab. We made several iterations before ending up with the final model. Eventually, we used PaDiM (Defard et al. 2020) for outlier detection, i.e. black images, or any image that differs significantly from the main distribution. We used Keras to implement the solution.

The project was interesting, of course from a deep learning point of view, since we get to code in classical frameworks and work on real data, but the main takeaway I get from it is the project management. The biggest challenge was more to coordinate all stakeholders than developping the model.

We provide the report as well as the repo for this project, unfortunately these are in French, so if you are not a speaker you might have to translate a couple things.

[🐈 Offical GitHub Repo](https://github.com/tristanscl/valeo_ai_challenge)

[📄 Report (PDF)](xxx)