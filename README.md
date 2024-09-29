# Tree Trunk Circumference Estimator Using QR Code Reference
This project estimates the circumference of a tree trunk using two images containing a QR code of known size. By identifying the QR code and tree trunk contours in the images, the script calculates the real-world width of the trunk and then uses Ramanujan's approximation to estimate the circumference of the tree trunk.

## Features

- Detects QR code and tree trunk contours in the provided images.
- Estimates tree trunk width based on the known size of the QR code.
- Computes the circumference of the tree trunk using two images.
- Displays visual feedback of detected QR code and tree trunk contours.

## Requirements

This script requires the following Python libraries:

- OpenCV
- NumPy

You can install these dependencies via pip:

bash

Copy code

`pip install opencv-python numpy`

## Usage

### 1. Input Images

You need two images of the tree trunk taken from different angles or distances, with a visible QR code placed near the tree trunk for scale reference. Ensure the QR code is square-shaped and its size is known.

### 2. Known QR Code Size

Modify the `qr_code_size_cm` parameter in the code with the real-world size (in centimeters) of the QR code.

### 3. Running the Script

Update the paths to your images in the code, then run the script as follows:

python

Copy code

`image_path1 = "img1.jpg"  # First image path image_path2 = "img2.jpg"  # Second image path qr_code_size_cm = 20.0    # Known size of QR code in centimeters  # Execute the script python script.py`

The script will display the images with the detected QR code and tree trunk boundaries and print the estimated circumference.

### 4. Visualization

Set the `display=True` argument in the `measure_object` function to view the image with highlighted contours for both the QR code and tree trunk.

### 5. Estimating Tree Trunk Circumference

The script uses two images of the same tree trunk and calculates the circumference using the semi-major and semi-minor axes (derived from the width in each image). The formula is based on Ramanujan's approximation for an ellipse.

### Example Output

mathematica

Copy code

`Estimated Circumference of the Tree Trunk: 125.34 cm`

## Code Structure

- **measure_object**: Detects and measures the tree trunk using the QR code for scale.
- **estimate_circumference**: Computes the tree trunk's circumference based on the trunk widths in two images.
- **resize_image**: Resizes images for display without upscaling.

## Error Handling

- If no QR code or tree trunk is found in the image, an error message will be raised.

## License

This project is licensed under the MIT License.

## Contributions

Feel free to contribute by creating issues or pull requests.