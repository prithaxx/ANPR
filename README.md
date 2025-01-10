# Number Plate Detection and Text Recognition

This project demonstrates how to detect a license plate in an image, extract it, and perform Optical Character Recognition (OCR) to read the text using OpenCV, EasyOCR, and Python.

## Requirements

Make sure you have the following installed:

### Python Packages
- Python 3.8 or later
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- Imutils
- EasyOCR

### Installation
Install the required Python packages using:
```bash
pip install opencv-python numpy matplotlib imutils easyocr
```

### Input File
Place the image file (e.g., `image4.jpg`) in a folder named `img` in the project directory. Ensure the file path in the code matches this location.

## How to Run the Code

1. Clone or download this repository.
2. Ensure your image file (e.g., `image4.jpg`) is placed in the `img/` folder.
3. Run the code using the following command:

```bash
python main.py
```

## Code Description

The script performs the following steps:

1. **Read the Input Image**
   - Load the image using OpenCV.

2. **Preprocess the Image**
   - Convert the image to grayscale.
   - Apply a bilateral filter to reduce noise while preserving edges.
   - Detect edges using the Canny edge detection method.

3. **Find Contours**
   - Extract contours from the edged image.
   - Sort the contours and find the best candidate with 4 sides (assumed to be the license plate).

4. **Extract the License Plate**
   - Mask the area of the detected license plate.
   - Crop the license plate region.

5. **Perform OCR**
   - Use EasyOCR to read the text on the license plate.

6. **Visualize the Results**
   - Display intermediate and final outputs using Matplotlib.

## Visualization Steps
- Grayscale Image
- Edged Image
- Masked Contour Image
- Cropped License Plate
- Final Image with Text Overlay

## Example Output
The script will generate several visual outputs and display them using Matplotlib. Ensure you have added `plt.show()` in the script to view them.


 
