# Docker Installation Guide for macOS, Windows, and Linux

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Docker Installation on macOS](#docker-installation-on-macos)
  - [1. Download Docker Desktop](#1-download-docker-desktop)
  - [2. Install Docker Desktop](#2-install-docker-desktop)
  - [3. Start Docker](#3-start-docker)
  - [4. Verify Installation](#4-verify-installation)
  - [5. Run a Test Container](#5-run-a-test-container)
- [Docker Installation on Windows](#docker-installation-on-windows)
  - [1. Download Docker Desktop](#1-download-docker-desktop-1)
  - [2. Install Docker Desktop](#2-install-docker-desktop-1)
  - [3. Start Docker](#3-start-docker-1)
  - [4. Verify Installation](#4-verify-installation-1)
  - [5. Run a Test Container](#5-run-a-test-container-1)
- [Docker Installation on Linux](#docker-installation-on-linux)
  - [1. Update Your Package Database](#1-update-your-package-database)
  - [2. Install Prerequisites](#2-install-prerequisites)
  - [3. Add Docker’s GPG Key](#3-add-dockers-gpg-key)
  - [4. Set Up the Stable Repository](#4-set-up-the-stable-repository)
  - [5. Install Docker](#5-install-docker)
  - [6. Verify Installation](#6-verify-installation)
  - [7. Run a Test Container](#7-run-a-test-container)

## Introduction
Docker is a platform that allows you to develop, ship, and run applications inside containers. Containers are lightweight and executable packages of software that include everything needed to run an application: code, runtime, system tools, libraries, and settings. This guide will walk you through the installation process of Docker on macOS, Windows, and Linux.

## Prerequisites
Before installing Docker, ensure your system meets the following requirements:

- **macOS**: macOS 10.15 or newer.
- **Windows**: Windows 10 64-bit: Pro, Enterprise, or Education (Build 19041 or higher).
- **Linux**: A 64-bit distribution running kernel version 3.10 or higher.

## Docker Installation on macOS

### 1. Download Docker Desktop
- Visit the [Docker Desktop for Mac](https://www.docker.com/products/docker-desktop) page.
- Click on "Download for Mac" to get the installer.

### 2. Install Docker Desktop
- Once the `.dmg` file is downloaded, double-click it to open.
- Drag the Docker icon to the Applications folder.

### 3. Start Docker
- Open the Docker application from the Applications folder.
- Docker will launch and ask for system permissions to install components.
- Enter your system password when prompted.

### 4. Verify Installation
- Open a terminal and run the command:
  ```bash
  docker --version
    ```

---

## Docker Installation on Windows

### 1. Download Docker Desktop
- Visit the [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop) download page.
- Click on the "Download for Windows" button.

### 2. Install Docker Desktop
- Run the installer and follow the on-screen instructions.
- Make sure to enable the option to use WSL 2 (Windows Subsystem for Linux) during the installation process.

### 3. Verify Installation
- Open Command Prompt or PowerShell and run:
    ```bash
    docker --version
    ```
- This should return the version of Docker installed.

### 4. Run a Test Container
- To verify Docker is working correctly, run:
    ```bash
    docker run hello-world
    ```
- This command downloads and runs a simple container that outputs a confirmation message.

---

## Docker Installation on Linux

### 1. Update Your Package Database
- Open a terminal and run:
    ```bash
    sudo apt-get update
    ```

### 2. Install Prerequisites
- Install necessary packages to allow apt to use a repository over HTTPS:
    ```bash
    sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
    ```

### 3. Add Docker’s GPG Key
- Add Docker’s official GPG key:
    ```bash
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    ```

### 4. Set Up the Stable Repository
- Use the following command to set up the stable repository:
    ```bash
    echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```

### 5. Install Docker
- Update the package database and install Docker:
    ```bash
    sudo apt-get update
    sudo apt-get install docker-ce docker-ce-cli containerd.io
    ```

### 6. Verify Installation
- Check if Docker is installed correctly:
    ```bash
    docker --version
    ```

### 7. Run a Test Container
- Run the following command to ensure Docker is functioning:
    ```bash
    sudo docker run hello-world
    ```

---
