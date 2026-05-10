# Landmark Transformer for Character-level Hand Sign Detection

An implementation of a transformer-based model inspired by "TSLFormer: A Lightweight Transformer Model for Turkish Sign Language Recognition Using Skeletal Landmarks"

## Dataset

Download Link: https://drive.google.com/file/d/1wGmuOAsRvzBy6YG6XhfGkvtX5WnzfUsS/view?usp=sharing

## Project Structure

- `dataset/`: Data storage (processed and augmented)
  - `images/`: Hand sign images
  - `labels.csv`: A csv that stores the images' name with their labels
- `checkpoints/`: Models' weights and their training history
- `results`: Models' training results (Train loss graph & prediction dataset for test set)
- `notebooks/`: Jupyter notebooks for exploration