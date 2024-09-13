# Colab, Conda, and Terminal Guide

This document will help you get started with:
1. [Using Google Colab for Python](#google-colab-for-python)
2. [Using R in Google Colab](#using-r-in-google-colab)
3. [Conda Installation in Google Colab](#conda-installation-in-google-colab)
4. [Using the Terminal in Google Colab](#using-the-terminal-in-google-colab)

---

## Google Colab for Python

Google Colab allows you to write and execute Python code in the cloud, with access to free GPUs and TPUs. Here’s a quick start guide for Python in Colab.

### 1. Opening Google Colab

- Go to [Google Colab](https://colab.research.google.com/).
- Select **File > New notebook** to create a new notebook.

### 2. Running Python Code

Create a code cell and run:

```python
print("Hello, Colab!")```

### 3. Using GPU/TPU
Enable GPU/TPU by going to **Runtime > Change runtime type** and selecting **GPU** or **TPU**.

---

## Using R in Google Colab

You can use R in Google Colab by installing the necessary packages and changing the runtime.

### 1. Installing R
In a code cell, run the following command to install R:

```bash
!apt-get install r-base```

