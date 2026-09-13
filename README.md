# Pencitraan Digital Assignment 01

## Image Downsampling and Upsampling
This project implements and compares six image-resampling algorithms in Python. It examines how reducing and enlarging an image affects edges, color transitions, fine details, and noise.

## Author

* **Name:** Farrel Anggito Baswara Marpaung
* **University:** University of Gadjah Mada
* **NIM:** 25/559096/PA/23506

## Algorithms

### Downsampling
Each method converts a 256 × 256 image into a 128 × 128 image using non-overlapping 2 × 2 blocks.
* **Max:** Selects the maximum value in each color channel.
* **Median:** Calculates the median value in each channel. For four samples, this averages the two middle values.
* **Average:** Calculates the arithmetic mean in each channel.

### Upsampling
Each method enlarges the average-downsampled image from 128 × 128 to 256 × 256.
* **Nearest Neighbor:** Copies source pixels into larger pixel blocks.
* **Bilinear:** Interpolates using four neighboring samples.
* **Bicubic:** Uses a cubic weighting function over a 4 × 4 neighborhood.

## Technologies
* Python
* NumPy
* OpenCV
* Matplotlib
* Google Colab

## Test Images
Three image types are used:
1. **Geometric image:** Examines sharp boundaries, shapes, and color transitions.
2. **Sunset photograph:** Examines natural gradients and fine leaf details.
3. **Salt-and-pepper noisy image:** Examines how each method handles extreme pixel values.

## How to Run
1. Open `PCD_Assignment01(1).ipynb` in Google Colab.
2. Run the initial upload cell and select a 256 × 256 test image.
3. Run the median, average, and max downsampling cells.
4. When the upsampling section requests another upload, select the same image.
5. Run the nearest neighbor, bilinear, and bicubic cells in order.
6. Repeat the experiment with the other test images.

note: 
The notebook uses Google Colab’s upload interface, so running it locally requires replacing the upload cells with local file loading.
