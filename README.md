# Landmark Transformer for Character-level Hand Sign Detection

An implementation of a transformer-based model inspired by "TSLFormer: A Lightweight Transformer Model for Turkish Sign Language Recognition Using Skeletal Landmarks"

## Dataset

Download Link: https://drive.google.com/file/d/1wGmuOAsRvzBy6YG6XhfGkvtX5WnzfUsS/view?usp=sharing

## Project Structure

- `dataset/`: Data storage (processed and augmented)
  - `images/`: Hand sign images
  - `labels.csv`: A csv that stores the images' name with their labels
  - `labels_with_landmarks.parquet`: A csv that stores the images' name with their labels and extracted MediaPipe landmarks
- `checkpoints/`: Models' weights and their training history
- `results`: Models' training results (Train loss graph & prediction dataset for test set)
- `notebooks/`: Jupyter notebooks for exploration and model training
  - `landmark_extractor.ipynb`: Preprocessing notebook for extracting MediaPipe Landmarks from the hand images
  - `model.ipynb`: The first version of the transformer model, a lot of of logics are kinda not practical but keep it just in case
  - `model_experiment_with_another_data.ipynb`: The latest improved Transformer Hand Sign Detection model pipeline, a lot better than the first version
- `hand_landmarker/`: A directory that stores Google's MediaPipe Hand model for use
