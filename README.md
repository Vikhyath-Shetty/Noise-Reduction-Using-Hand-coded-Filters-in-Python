**To Open the notebook on google collab, Click on the below badge:**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Vikhyath-Shetty/Noise-Reduction-Using-Hand-coded-Filters-in-Python/blob/master/Noise%20Reduction%20Using%20Hand-Coded%20Filters%20in%20Python.ipynb)

# 🧹 Noise Reduction Using Mean and Median Filters

This project demonstrates how to **reduce noise from images** using two classic image processing techniques:  
✔️ **Mean Filter**  
✔️ **Median Filter**  

Both filters are implemented **from scratch in Python using NumPy**, without using OpenCV or other image-processing libraries.

---

## 📁 Folder Contents
- `Noise Reduction using handcoded filters in python.ipynb`: Main notebook containing code, explanations, and output images.
- `girl_noisy_image.jpeg`: Input image with noise.
- `sculpt_noisy_image.jpeg`: Input image with noise.


---

## 🧠 What Are These Filters?

### 🟦 Mean Filter
Averages the surrounding pixels in a kernel to smooth out noise.  
⚠️ May blur edges.

> The function `mean_filter()` applies mean filtering to an RGB image using a specified kernel size.  
> It replaces each pixel with the **average value** of its neighborhood, resulting in a **blurring effect** that helps **reduce general noise**.  
>  
> Unlike using built-in functions from libraries like OpenCV, this implementation is done **completely from scratch**, iterating manually with NumPy.

---

### 🟨 Median Filter
Replaces each pixel with the **median** of its neighbors, which better preserves edges while removing salt-and-pepper noise.

> The function `median_filter()` applies median filtering to an RGB image using a specified kernel size.  
> It replaces each pixel with the **median value** from its local neighborhood, effectively removing impulse noise while **preserving important features and edges**.  
>  
> Like the mean filter, this is a **fully manual implementation using NumPy**.

---

## 🔧 How It Works

1. Load the image (supports both file path or PIL Image object).
2. Convert it to a NumPy matrix.
3. Pad the matrix to handle edges.
4. Slide a `ker x ker` window over each pixel.
5. Replace the center pixel with the mean or median of the window.
6. Save or return the filtered image.

---

