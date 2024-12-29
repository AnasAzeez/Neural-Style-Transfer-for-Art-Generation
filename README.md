# Neural Style Transfer for Art Generation

This repository contains an implementation of Neural Style Transfer using TensorFlow. The script allows users to generate new images by blending the content of one image with the artistic style of another.

## Features

- **Content and Style Cost Computation**: Implements the calculation of content and style costs based on VGG19 feature maps.
- **Style Layers**: Allows selection of multiple layers for extracting style features.
- **Gradient Descent Optimization**: Iteratively updates the generated image to minimize total cost.
- **Output Visualizations**: Displays the content image, style image, and generated image side by side.

## Prerequisites

- Python 3.7+
- TensorFlow 2.0+
- Required Python libraries: `numpy`, `Pillow`, `matplotlib`, `scipy`

Install the dependencies using:

```bash
pip install tensorflow numpy pillow matplotlib scipy
```

## Usage

1. **Dataset Preparation**:
   - Place the content image (e.g., `louvre.jpg`) in the `images/` directory.
   - Place the style image (e.g., `monet.jpg`) in the same directory.

2. **Run the Script**:
   - Execute the `Art_Generation_with_Neural_Style_Transfer.py` script.
   - The script preprocesses images, calculates style and content costs, and generates a new image using gradient descent.

3. **Configuration**:
   - Modify the following parameters in the script if necessary:
     - `img_size`: Size of input images (default: 400).
     - `epochs`: Number of training iterations (default: 2501).
     - `alpha`, `beta`: Weights for content and style costs (default: 10, 40).

4. **Output**:
   - The generated images are saved in the `output/` directory at intervals (e.g., `image_0.jpg`, `image_250.jpg`).

## How It Works

- **VGG19 Pretrained Model**: Uses the VGG19 network to extract content and style features.
- **Content Cost**: Captures similarity between the content image and the generated image.
- **Style Cost**: Measures differences in Gram matrices between the style image and the generated image.
- **Optimization**: Minimizes the weighted sum of content and style costs using gradient descent.

## Example Results

During the optimization process, the script outputs intermediate images, demonstrating how the generated image evolves to blend content and style. Here is an example of the output:

- **Content Image**: Louvre museum
- **Style Image**: Monet painting
- **Generated Image**: A stylized version of the Louvre image

## License

This project is licensed under the MIT License.

