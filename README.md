# Landmark Transformer for Character-level Hand Sign Detection

An implementation of a transformer-based model inspired by "TSLFormer: A Lightweight Transformer Model for Turkish Sign Language Recognition Using Skeletal Landmarks"

## Dataset Acknowledgements

This project utilizes two primary datasets sourced from Kaggle:

**ASL Alphabet Dataset**: Provided by [Amey Thakur](https://www.kaggle.com/datasets/ameythakur20/asl-alphabet-test). This dataset was used for training alphabet characters (A-Z).

**Hand Sign Gesture Dataset (AZ & 09)**: Provided by [Debabrata Kuiry](https://www.kaggle.com/datasets/debabratakuiry/hand-sign-gesture-dataset-az-and-09-25k-images). This dataset provided the numerical characters (0-9) and additional gesture samples.

All data is used in accordance with the licenses provided by the respective authors on the Kaggle platform.

**Augmented Dataset from our method Download Link**: https://drive.google.com/file/d/1wGmuOAsRvzBy6YG6XhfGkvtX5WnzfUsS/view?usp=sharing

## Project Structure

- `dataset/`: Data storage (processed and augmented)
  - `images/`: Hand sign images (this directory is hidden and needs to be downloaded from the link)
  - `labels.csv`: A csv that stores the images' name with their labels
  - `labels_with_landmarks_v2.parquet`: A csv that stores the images' name with their labels and extracted MediaPipe landmarks
- `checkpoints/`: Models' weights and their training history
- `results`: Models' training results (Loss graph, Accuracy graph & Confusion Matrix)
- `notebooks/`: Jupyter notebooks for exploration and model training
  - `landmark_extractor.ipynb`: Preprocessing notebook for extracting MediaPipe Landmarks from the hand images
  - `model.ipynb`: The first version of the transformer model, a lot of of logics are kinda not practical but keep it just in case
  - `model_experiment_with_another_data.ipynb`: The latest improved Transformer Hand Sign Detection model pipeline, a lot better and more practical than the first version
- `hand_landmarker/`: A directory that stores Google's MediaPipe Hand model for use

## Third Party Model Acknowledgements

This project utilizes the [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) model developed by Google. 
