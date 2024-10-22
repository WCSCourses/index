# Google Colab Guide

[Wellcome Connecting Science GitHub Home Page](https://github.com/WCSCourses) <br /> 
[Wellcome Connecting Science Website](https://coursesandconferences.wellcomeconnectingscience.org/)

## Table of Contents:
1. [What is Google Colab?](#what-is-google-colab)
2. [How Does Google Colab Work?](#how-does-google-colab-work)
3. [Getting Started with Google Colab](#getting-started-with-google-colab)
4. [Using Google Colab for Python](#google-colab-for-python)
5. [Using R in Google Colab](#using-r-in-google-colab)
6. [Conda Installation in Google Colab](#conda-installation-in-google-colab)
7. [Using the Terminal in Google Colab](#using-the-terminal-in-google-colab)
8. [Helpful Links](#helpful-links)
9. [Helpful Communities](#helpful-communities)

## What is Google Colab?

Google Colab, or "Collaboratory," is a cloud-based platform that allows you to write and execute Python code in a web browser. It is particularly popular for data analysis, machine learning, and artificial intelligence projects because it provides free access to powerful computing resources, including GPUs and TPUs.

## How Does Google Colab Work?

Google Colab integrates seamlessly with Google Drive, making it easy to save and share your notebooks. Each notebook consists of code cells and text cells, allowing you to combine code, comments, and visualizations. Colab supports various Python libraries and frameworks, enabling you to run code without needing to set up a local environment.

Key features of Google Colab include:

- **Free Access to GPUs/TPUs:** You can leverage powerful hardware for your computations without any cost.
- **Collaboration:** Multiple users can work on the same notebook in real time, similar to Google Docs.
- **Pre-installed Libraries:** Colab comes with many popular libraries pre-installed, such as TensorFlow, NumPy, and Pandas.
- **Easy Integration:** You can easily import datasets from Google Drive, GitHub, and other sources.

## Getting Started with Google Colab

To get started with Google Colab using a shared link from Google Drive:

1. **Open the Shared Link:** Click on the shared link provided to you. It will usually look like this: `https://drive.google.com/file/d/...`.
   
2. **Make a Copy:** If the link opens a view-only version of the notebook, you can create your own editable copy by selecting **File > Save a copy in Drive**. This will save the notebook to your Google Drive.

3. **Open Your Copy:** Once the copy is saved, you can open it from your Google Drive. You can also access it anytime through Google Colab by selecting **File > Open notebook** and navigating to your Drive.

---

## Google Colab for Python

Google Colab allows you to write and execute Python code in the cloud, with access to free GPUs and TPUs. Here’s a quick start guide for Python in Colab.

### 1. Opening Google Colab

- Go to [Google Colab](https://colab.research.google.com/).
- Select **File > New notebook** to create a new notebook.

### 2. Running Python Code

Create a code cell and run:

```python
print("Hello, Colab!")
```
### 3. Using GPU/TPU
Enable GPU/TPU by going to **Runtime > Change runtime type** and selecting **GPU** or **TPU**.

---

### Using R in Google Colab
You can use R in Google Colab by installing the necessary packages and changing the runtime.

#### 1. Installing R
In a code cell, run the following command to install R:

```bash
!apt-get install r-base
```
#### 2. Running R Code
After installing R, you can run R code by prefixing your code cell with %%R. For example:

```bash
%%R
print("Hello, R in Colab!")
```

---

### Conda Installation in Google Colab
You can install Conda in Google Colab to manage your Python packages and environments. Follow these steps:

#### 1. Install Miniconda
In a code cell, run the following command to install Miniconda:

```bash
!wget -qO- https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh | bash
```

#### 2. Initialize Conda
After installation, initialize Conda with:

```bash
import sys
!conda init
```

#### 3. Creating a Conda Environment
Create a new environment by running:

```bash
!conda create --name myenv python=3.8
```

#### Activate the environment:

```bash
!source activate myenv
```

---
### Using the Terminal in Google Colab
You can access the terminal in Google Colab by using the following command:

#### 1. Open Terminal
In a code cell, run:

```bash
!bash
```
This will open a terminal session where you can execute standard Linux commands.

#### 2. Running Commands
You can run any command as you would in a typical terminal environment. For example:

```bash
ls
```
---

## Helpful Links

- [Google Colab Documentation](https://colab.research.google.com/notebooks/welcome.ipynb)  
  Official documentation to help you get started with Google Colab.

- [Google Colab FAQ](https://research.google.com/colaboratory/faq.html)  
  Frequently asked questions about Google Colab, covering common issues and tips.

- [Learn Python with Google Colab](https://colab.research.google.com/notebooks/python_intro.ipynb)  
  A beginner-friendly tutorial to help you learn Python directly in Colab.

- [Getting Started with R in Google Colab](https://towardsdatascience.com/getting-started-with-r-in-google-colab-f5bc034c81f6)  
  A guide for using R in Google Colab, including installation and running R code.

Feel free to reach out if you have any questions or need further assistance!

---

## Helpful Communities

- [Stack Overflow](https://stackoverflow.com/questions/tagged/google-colaboratory)  
  A large community for developers and data scientists to ask questions about Google Colab.

- [Google Colab Community on Reddit](https://www.reddit.com/r/GoogleColab/)  
  A subreddit for discussions, tips, and solutions related to Google Colab.

- [Kaggle Forums](https://www.kaggle.com/)  
  Kaggle hosts discussions on a variety of machine learning and data science topics, including using Google Colab for competitions.

- [Data Science Stack Exchange](https://datascience.stackexchange.com/questions/tagged/google-colab)  
  A Q&A community for data science, where you can ask about issues related to Google Colab and other tools.

Join these communities to connect with others, get support, and share your experiences with Colab.

---

[Wellcome Connecting Science GitHub Home Page](https://github.com/WCSCourses) 

For more information or queries, feel free to contact us via the [Wellcome Connecting Science website](https://coursesandconferences.wellcomeconnectingscience.org).<br /> 
Find us on socials [Wellcome Connecting Science Linktr](https://linktr.ee/eventswcs)

---
