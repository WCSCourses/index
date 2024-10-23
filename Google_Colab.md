# Google Colab Guide

[Wellcome Connecting Science GitHub Home Page](https://github.com/WCSCourses) <br /> 
[Wellcome Connecting Science Website](https://coursesandconferences.wellcomeconnectingscience.org/)

## Table of Contents
1. [What is Google Colab?](#1-what-is-google-colab)
2. [How Does Google Colab Work?](#2-how-does-google-colab-work)
3. [Getting Started with Google Colab](#3-getting-started-with-google-colab)
4. [Using Google Colab for Python](#4-using-google-colab-for-python)  
   a. [Opening Google Colab](#a-opening-google-colab)  
   b. [Running Python Code](#b-running-python-code)  
   c. [Using GPU/TPU](#c-using-gputpu)  
5. [Using R in Google Colab](#5-using-r-in-google-colab)  
   a. [Installing R](#a-installing-r)  
   b. [Running R Code](#b-running-r-code)  
6. [Conda Installation in Google Colab](#6-conda-installation-in-google-colab)  
   a. [Install Miniconda](#a-install-miniconda)  
   b. [Initialize Conda](#b-initialize-conda)  
   c. [Creating a Conda Environment](#c-creating-a-conda-environment)  
7. [Using the Terminal in Google Colab](#7-using-the-terminal-in-google-colab)  
   a. [Open Terminal](#a-open-terminal)  
   b. [Running Commands](#b-running-commands)  
8. [Managing Files in Google Colab](#8-managing-files-in-google-colab)  
 a. [Different Ways to Add Files in Google Colab](#a-different-ways-to-add-files-in-google-colab)  
      - [Upload from Local Machine](#upload-from-local-machine)  
      - [Mount Google Drive](#mount-google-drive)  
      - [Use GitHub Repositories](#use-github-repositories)  
      - [Download from a URL](#download-from-a-url) </br>
 b. [Zipping Files](#b-zipping-files)  
 c. [Unzipping Files](#c-unzipping-files)  
 d. [Adding Data Before Zipping](#d-adding-data-before-zipping)  
10. [Google Colab Frequently Asked Questions (FAQs)](#9-google-colab-frequently-asked-questions-faqs)
11. [Helpful Links](#10-helpful-links)
12. [Helpful Communities](#11-helpful-communities)


## 1. What is Google Colab?

Google Colab, or "Collaboratory," is a cloud-based platform that allows you to write and execute Python code in a web browser. It is particularly popular for data analysis, machine learning, and artificial intelligence projects because it provides free access to powerful computing resources, including GPUs and TPUs.

## 2. How Does Google Colab Work?

Google Colab integrates seamlessly with Google Drive, making it easy to save and share your notebooks. Each notebook consists of code cells and text cells, allowing you to combine code, comments, and visualizations. Colab supports various Python libraries and frameworks, enabling you to run code without needing to set up a local environment.

Key features of Google Colab include:

- **Free Access to GPUs/TPUs:** You can leverage powerful hardware for your computations without any cost.
- **Collaboration:** Multiple users can work on the same notebook in real time, similar to Google Docs.
- **Pre-installed Libraries:** Colab comes with many popular libraries pre-installed, such as TensorFlow, NumPy, and Pandas.
- **Easy Integration:** You can easily import datasets from Google Drive, GitHub, and other sources.

## 3. Getting Started with Google Colab

To get started with Google Colab using a shared link from Google Drive:

a. **Open the Shared Link:** Click on the shared link provided to you. It will usually look like this: `https://drive.google.com/file/d/...`.
   
b. **Make a Copy:** If the link opens a view-only version of the notebook, you can create your own editable copy by selecting **File > Save a copy in Drive**. This will save the notebook to your Google Drive.

c. **Open Your Copy:** Once the copy is saved, you can open it from your Google Drive. You can also access it anytime through Google Colab by selecting **File > Open notebook** and navigating to your Drive.

---

## 4. Using Google Colab for Python

Google Colab allows you to write and execute Python code in the cloud, with access to free GPUs and TPUs. Here’s a quick start guide for Python in Colab.

### a. Opening Google Colab

- Go to [Google Colab](https://colab.research.google.com/).
- Select **File > New notebook** to create a new notebook.

### b. Running Python Code

Create a code cell and run:

```python
print("Hello, Colab!")
```
### c. Using GPU/TPU
Enable GPU/TPU by going to **Runtime > Change runtime type** and selecting **GPU** or **TPU**.

---

### 5. Using R in Google Colab
You can use R in Google Colab by installing the necessary packages and changing the runtime.

#### a. Installing R
In a code cell, run the following command to install R:

```bash
!apt-get install r-base
```
#### b. Running R Code
After installing R, you can run R code by prefixing your code cell with %%R. For example:

```bash
%%R
print("Hello, R in Colab!")
```

---

### 6. Conda Installation in Google Colab
You can install Conda in Google Colab to manage your Python packages and environments. Follow these steps:

#### a. Install Miniconda
In a code cell, run the following command to install Miniconda:

```bash
!wget -qO- https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh | bash
```

#### b. Initialize Conda
After installation, initialize Conda with:

```bash
import sys
!conda init
```

#### c. Creating a Conda Environment
Create a new environment by running:

```bash
!conda create --name myenv python=3.8
```

#### d. Activate the environment:

```bash
!source activate myenv
```

---
### 7. Using the Terminal in Google Colab
You can access the terminal in Google Colab by using the following command:

#### a. Open Terminal
In a code cell, run:

```bash
!bash
```
This will open a terminal session where you can execute standard Linux commands.

#### b. Running Commands
You can run any command as you would in a typical terminal environment. For example:

```bash
ls
```
---

## 8. Managing Files in Google Colab

#### a. Different Ways to Add Files in Google Colab
#### Upload from Local Machine:

To upload files directly from your local machine to Google Colab, use the following code:

```bash
from google.colab import files
uploaded = files.upload()
```

#### Mount Google Drive: 

You can mount your Google Drive to access files stored there. Use the following code to do this:

```bash
from google.colab import drive
drive.mount('/content/drive')
```
After executing this, you’ll need to follow the authorization steps. Once mounted, you can access your Google Drive files under the /content/drive directory.

#### Use GitHub Repositories:

You can clone a GitHub repository to access files directly. Use the following command:

```bash
!git clone https://github.com/username/repo.git
```
Replace the username and repo with the appropriate GitHub username and repository name.

#### Download from a URL:

If you have a direct link to a file, you can use wget or curl to download it:
```bash
!wget 'http://example.com/path/to/file'
```
or

```bash
!curl -O 'http://example.com/path/to/file'
```

#### b. Zipping Files 
You can zip files or folders in Google Colab using the following command:

```bash
!zip -r '/content/folder/filename.zip' /path/to/folder
```
This will create a zip file called filename.zip in the /content/folder/ directory.

#### c. Unzipping Files
To unzip a file in Google Colab, use the following command:

```bash
!unzip /path/to/file.zip
```
This will extract the contents of the zip file.

#### d. Adding Data Before Zipping
To add data to a zip file, move the necessary files or directories into a folder, and then zip the entire folder. For example:

```bash
!mkdir /content/folder
!cp /path/to/file /content/folder
!zip -r '/content/folder/filename.zip' /content/folder
```
This will copy the file to a folder and then zip the entire folder.

### 9. Google Colab Frequently Asked Questions (FAQs)

Q: How long can I run my notebook?
A: The maximum runtime per session is 12 hours. You can restart the session if needed.

Q: What happens if I leave my notebook idle?
A: After 90 minutes of inactivity, Colab will stop the session. You will need to reconnect and rerun your code.

Q: Can I save my work if my session stops?
A: Yes, save your notebooks to Google Drive or manually download files before the session expires.

Q: Can I increase the runtime limit?
A: Google Colab has a fixed runtime limit of 12 hours per session. You cannot extend this limit, but you can reconnect and restart the session.

---
## 10. Helpful Links

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

## 11. Helpful Communities

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
