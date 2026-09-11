# Image Sharpening & Deblurring using OpenCV

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-green?style=for-the-badge&logo=opencv" alt="OpenCV">
  <img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-orange?style=for-the-badge&logo=numpy" alt="NumPy">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter" alt="Jupyter">
</p>

<p align="center">
  <b>Enhancing blurry images using spatial-domain image sharpening techniques.</b>
</p>

---

##  Overview

This project explores **image sharpening and enhancement** using Python and OpenCV.

The objective is to take a blurry input image and enhance its edges and fine details using convolution-based sharpening filters.

The implementation is provided as a Jupyter Notebook and demonstrates the image-processing workflow from loading the image to applying a sharpening kernel and visualizing the result.

---

##  Objective

> **Perform image sharpening on blurry images.**

The project focuses on improving the visual clarity of blurred images by emphasizing high-frequency components such as:

* 🔹 Edges
* 🔹 Fine details
* 🔹 Object boundaries
* 🔹 Texture information

---

##  Concept

Image sharpening can be performed using a convolution kernel that increases the contribution of the center pixel while subtracting neighboring pixel information.

A typical sharpening kernel is:

```text
[ 0  -1   0 ]
[-1   5  -1 ]
[ 0  -1   0 ]
```

The kernel enhances intensity transitions, making edges appear sharper.

Mathematically, the filtered image can be represented as:

$$
I_{sharp} = I * K
$$

where:

* \(I\) = input image
* \(K\) = sharpening kernel
* \(*\) = convolution operation
* \(I_{sharp}\) = sharpened image

---

##  Methodology

The image-processing pipeline follows these steps:

```text
             ┌──────────────────┐
             │   Blurry Image   │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │   Read Image     │
             │    using OpenCV  │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Create Sharpening│
             │      Kernel      │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │  2D Convolution  │
             │    filter2D()    │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Sharpened Image  │
             └──────────────────┘
```

---

##  Technologies Used

| Technology          | Purpose                                |
| ------------------- | -------------------------------------- |
|  Python             | Programming language                   |
|  OpenCV             | Image processing                       |
|  NumPy              | Kernel creation & numerical operations |
|  Jupyter Notebook   | Implementation & experimentation       |
|  Matplotlib         | Image visualization                    |

| <img src="images/original.jpg" width="450"> | <img src="images/blurred.jpg" width="450"> |


The notebook imports OpenCV, NumPy, and Matplotlib for the image-processing workflow.

---


> **Note:** Sharpening does not truly recover information that was completely lost during image acquisition. It primarily enhances existing edges and high-frequency information.

---

##  Understanding the Result

A successful sharpening operation should generally produce:

**Before**

```text
Blurred edges
      ↓
Reduced detail
      ↓
Low visual sharpness
```

**After**

```text
Enhanced edges
      ↓
Stronger intensity transitions
      ↓
Improved perceived sharpness
```

However, excessive sharpening can introduce:

*  Noise amplification
*  Halo artifacts
*  Oversharpened edges
*  Unnatural appearance

Therefore, the sharpening kernel needs to be selected carefully.

---

##  Project Structure

```text
Image-Sharpening/
│
├──  Sharpening.ipynb
├──  images/
│   ├── blurry/
│   └── output/
│
├──  README.md
└──  requirements.txt
```

---

##  Installation

Clone the repository:

```bash
git clone <REPOSITORY_URL>
cd Image-Sharpening
```

Install the required packages:

```bash
pip install opencv-python numpy matplotlib
```

Or:

```bash
pip install -r requirements.txt
```

### `requirements.txt`

```text
opencv-python
numpy
matplotlib
```

---

##  How to Run

### Using Jupyter Notebook

```bash
jupyter notebook sharpening.ipynb
```

Then execute the notebook cells sequentially.

### Using Google Colab

Upload `sharpening.ipynb` to Google Colab and run the cells.

---

##  Experiment

This notebook is part of an image-processing exercise focused on **image enhancement through spatial filtering**.

The experiment demonstrates how convolution-based filters can modify an image and improve its perceived sharpness.

---

##  Possible Improvements

The project can be extended by experimenting with:

*  Different sharpening kernels
*  Adjustable sharpening strength
*  Gaussian blur removal
*  Unsharp masking
*  Laplacian sharpening
*  Canny edge detection
*  Quantitative image-quality metrics
*  Deep-learning-based image deblurring

A particularly useful extension is comparing different sharpening techniques quantitatively instead of relying only on visual inspection.

---

##  Key Takeaways

* Image sharpening enhances **edges and fine details**.
* Convolution kernels can be used to perform spatial-domain sharpening.
* OpenCV's `filter2D()` provides a simple way to apply custom filters.
* Strong sharpening can also amplify image noise.
* Visual quality and quantitative metrics should both be considered when evaluating enhancement techniques.

---

##  Author

**Chitrarth**

> Computer Vision • Image Processing • Python • OpenCV

---

##  If You Found This Useful

If this project helped you understand image sharpening or OpenCV filtering, consider giving the repository a ⭐!

---

<p align="center">
  <b>Built with Python & OpenCV  </b>
</p>

