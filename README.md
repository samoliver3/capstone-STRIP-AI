# Predicting Acute Ischemic Stroke Etiology from Whole Slide Digital Pathology Imaging of Clot Composition Retrieved via Mechanical Thrombectomy

Created by Sam Oliver

## Project Overview

In the United States, over 700,000 people suffer an ischemic stroke every year, and stroke is the second most common cause of death in the world. Around 25% of people that have a stroke suffer one or more additional strokes. Identifying stroke etiology improves the likelihood of survival. Stroke Thromboembolism Registery of Imaging and Pathology (STRIP) is a project run by the Mayo Clinic Neurovascular Lab across multiple centers with the following goal: histopathologic characterization of thromboemboli of various etiologies and examining clot composition and its relation to mechanical thrombectomy revascularization. This project will take advantage of resources collected by STRIP to predict stroke etiology (the origin of the stroke). The task of this project is to predict whether a stroke ocurred as one or the other of the main two acute iscehmic stroke etiology subtypes: cardioembolic (CE) or large artery atherosclerosis (LAA). This prediction will be carried out using deep convolutional neural networks that will input images of blood clots that have been extracted from the brain of the patients in this dataset. At this point, it is helpful to define some of the terms noted in this introductory paragraph.

![diagram](./images/stroke_diagram.png)

Acute ischemic stroke (AIS): An ischemic stroke refers to a blood clot that blocks or narrows an artery leading to the brain. Acute, in this context, refers to a sudden medical episode related to a pre-existing condition.
Cardioembolic AIS: commonly defined as cerebral vessel occlusion by distant embolization arising from thrombus formation in the heart. CE is essentially the blocking of blood flow in the brain caused by a blood clot in the heart (coronary thrombosis).
Large Artery Atherosclerosis AIS: Atherosclerosis - changes in the walls of blood vessels that occur as a result of inflammation and the accumulation of fatty deposits. Atherosclerosis causes arteries to narrow, which impedes blood flow. Atherosclerotic plaque buildup can then rupture and cause the formation of blood clots that can block arteries in the brain, which can then cause stroke.

To reiterate, the goal of this project is to create useful predictions as to whether a stroke occurred from a clot in the heart or froom large artery atherosclerosis from an image of the removed blood clot from the patient's brain. The point of solving this project is to utizile beneficial prediction methods to then appropriately prescribe therapeutic treatmeant for patients that have suffered one of these kinds of strokes, which allows for more specialized treatment depending on which kind of stroke the patient had and will increase survival odds for the patient.

## The Stakeholder

The stakeholder is the Mayo Clinic, which is offering cash rewards to the creators of the top five best-scoring entries according to a scoring algorithm. The Mayo Clinic is asking for entries to classify images into one of the two major AIS categories for each image in a test set. These two major categories include Cardioembolic (CE) strokes and Large Artery Atherosclerosis (LAA) strokes.

## Navigation Instructions

This project utilizes two Jupyter Notebooks for all the code and data exploration used throughout the project. One of these notebooks was hosted on Google Colab, and this notebook created an allowance of more computational resources that could not be sourced from my own computer. Google Colab allowed for the use of more advanced GPUs and TPUs as well as approximately 32GB of RAM. These resources represent much greater computational capacities than my own machine. The other notebook utilized my own machine. This project also includes some PDFs for the Github repository, the notebooks, and a slideshow of the main findings for this project. This project utilized data from a Kaggle competition run by the Mayo Clinic. This project utilizes the original data provided by the Mayo Clinic as well as other datasets compiled by Kaggle users that were used in order to avoid OOM issues and other issues encountered by the large file sizes of the original images. Links to these datasets and other resources are below.

## Links to Important Resources

1. [Project Presentation]()
2. [Modeling and data exploration carried out on Google Colab](https://github.com/samoliver3/capstone-STRIP-AI/blob/main/STRIP.ipynb)
3. [Modeling and data exploration carried out by local machine](https://github.com/samoliver3/capstone-STRIP-AI/blob/main/og_data_modeling.ipynb)
4. [Original dataset provided by the Mayo Clinic on Kaggle](https://www.kaggle.com/competitions/mayo-clinic-strip-ai/data)
5. [Downsized png dataset](https://www.kaggle.com/datasets/jirkaborovec/stroke-blood-clot-origin-1k-scale-bg-crop)
6. [Tiled dataset](https://www.kaggle.com/datasets/tr1gg3rtrash/mayo-clinic)

## The Data

The dataset provided by the Mayo Clinic contains over a thousand high-resolution whole-slide digital pathology images. Each slide depicts a blood clot from a patient that had experienced an acute ischemic stroke. The dataset contains roughly a 2:1 ratio of CE to LAA blood clots. Some patients have multiple representations of blood clots in the dataset, and there are 11 different clinics that have contributed to the image registry.

![metadata](./images/metadata.png)

A preview of some of the images from each category (CE and LAA) can be seen below.

![imgs](./images/CE_LAA.png)
