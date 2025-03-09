# Spotify genre prediction

## Authors
Miguel Bande, Octavian Rotita

## Overview
This project focuses on predicting music genres using machine learning techniques. The dataset used is extracted from Spotify and made available on Kaggle. The project explores different classification approaches, including multi-class and multi-label classification, utilizing models such as Random Forest and Neural Networks.

## Table of Contents
- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Multi-class Classification](#multi-class-classification)
- [Multi-label Classification](#multi-label-classification)
- [Results](#results)
- [Future Work](#future-work)

## Introduction
With the digital transformation of music consumption, platforms like Spotify leverage machine learning algorithms to provide personalized recommendations. Organizing music by genre is crucial for recommendations, trend analysis, and content management. This project aims to classify songs into appropriate genres using machine learning techniques.

## Data Preprocessing
The dataset consists of 114,000 tracks with 21 features, including audio attributes like danceability, energy, loudness, and valence. The preprocessing steps include:
- Handling missing values and duplicate tracks.
- Feature selection and transformation.
- Reduction of the number of genres from 114 to broader categories.
- Splitting the dataset into training (80%) and testing (20%).

## Multi-class Classification
Initially, the problem is approached as a single-label classification task where each song belongs to only one genre. Models applied:
- **Random Forest:** Achieved an accuracy of approximately 54%.
- **Neural Network:** Implemented with three hidden layers, dropout regularization, and categorical cross-entropy loss.
- **PCA + Clustering:** Attempted dimensionality reduction and clustering but did not yield coherent genre groupings.

## Multi-label Classification
Given that songs can belong to multiple genres, a multi-label classification approach was implemented. Two methods were evaluated:
1. **Neural Network:** Applied sigmoid activation for multi-label classification, but results were unsatisfactory due to class imbalance.
2. **One vs The Rest (OvR):** Trained separate binary classifiers for each genre using Random Forest. This approach improved classification performance and provided better genre predictions.

## Results
- The **One vs The Rest (OvR)** method yielded the best results, successfully classifying songs into multiple genres based on probability thresholds.
- The deep learning approach struggled due to genre overlaps and data imbalance.
- Feature selection and data transformation played a crucial role in improving model performance.

## Future Work
- **Feature Engineering:** Use spectral analysis and advanced audio representations.
- **Deep Learning Approaches:** Implement Convolutional Neural Networks (CNNs) on spectrograms for better genre classification.
- **Time-based Analysis:** Consider how genre trends evolve over time using temporal modeling.
