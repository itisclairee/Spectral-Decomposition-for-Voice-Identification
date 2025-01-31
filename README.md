# Spectral-Decomposition-for-Voice-Identification

## Overview

Text Independent Speaker Identification is the task of identifying and separating individual speakers in a given audio sample. This technique is widely used in various fields, including banking and home security services, as a means of verifying user identity beyond traditional methods.
Unlabeled voice registrations serve as input for a model designed to identify different voices based on their unique characteristics. The resulting voice dictionary can then be compared with new samples to determine the speaker's identity.

## Dataset

The dataset used in this project was sourced from the OpenSLR project at the following link: [OpenSLR Dataset](https://www.openslr.org/45/). It was uploaded by the Surfingtech Company, which extracted it from a larger private dataset. The dataset consists of short audio samples for 10 speakers, with approximately 350 recordings per speaker in .wav format. To optimize computational efficiency, a subset of the dataset was used:

Training set: The first 20 recordings per speaker (totaling 200 training samples).
Testing set: The next 5 recordings per speaker (totaling 50 testing samples).

## Methodology

One common approach to speaker identification is to extract the frequency spectrum of the audio sample and apply a Gaussian Mixture Model (GMM) to distinguish different speakers.

### Feature Extraction

Raw audio samples cannot be directly used for GMM fitting and prediction. Instead, signal processing techniques are applied to extract meaningful features. In this project, the Mel-Frequency Cepstrum (MFC) is used for feature extraction.

