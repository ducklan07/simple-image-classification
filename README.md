# Identify Dog - Image Classification Project

This project uses Python and fastai to build a simple image classifier that distinguishes between images of dogs and forests. It demonstrates how to collect image data, preprocess it, train a deep learning model, and make predictions.

## Features

- **Automatic image download** using DuckDuckGo search
- **Data cleaning** to remove failed or corrupt images
- **Image resizing** for consistent input size
- **Model training** using fastai and a pretrained CNN (default: ResNet18)
- **Prediction** on new images

## Requirements

- Python 3.8+
- [fastai](https://docs.fast.ai/)
- [fastdownload](https://github.com/fastai/fastdownload)
- [duckduckgo-search](https://pypi.org/project/duckduckgo-search/)
- fastcore

Install dependencies with:

```bash
pip install fastai fastdownload duckduckgo-search fastcore
```

## How It Works

1. **Check Internet Connection:**  
   The notebook first checks for an active internet connection.

2. **Download Images:**  
   - Downloads a sample dog and forest image for testing.
   - Downloads up to 200 images each for "dog" and "forest" categories into `dog_or_not/dog` and `dog_or_not/forest`.

3. **Clean Data:**  
   - Removes failed or incomplete downloads (e.g., `.jpg!d` files).
   - Verifies that all images can be opened.

4. **Count Images:**  
   - Prints the number of valid images in each category.

5. **Prepare Data:**  
   - Creates a fastai `DataBlock` for image classification.
   - Splits data into training and validation sets (default: 80% train, 20% validation).

6. **Train Model:**  
   - Trains a convolutional neural network (default: ResNet18) to classify images.

7. **Make Predictions:**  
   - Tests the trained model on a sample image and prints the result.

## Usage

Open `main.ipynb` in Jupyter Notebook or VS Code and run the cells in order.

## Customization

- To use a different model, change `resnet18` to another supported model (e.g., `resnet34`, `efficientnet_b0`).
- To change the categories, modify the `searches` tuple.
- Adjust `max_images` in `search_images` to download more or fewer images.

## Notes

- Image downloads depend on DuckDuckGo search results and may vary.
- Some images may fail to download or be corrupt; the notebook includes steps to clean these up.
- Training accuracy depends on the quality and quantity of images.

---

**Author:**  
Declan Ng
2025
