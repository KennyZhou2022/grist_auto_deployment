# Custom Grist & Grist-Omnibus Docker Images

This repository contains GitHub Actions workflows for building and automatically pushing customized Docker images based on:

- `gristlabs/grist`
- `gristlabs/grist-omnibus`

Both images include additional Python packages and are published to Docker Hub under:

- **kenny2023/grist**
- **kenny2023/grist-omnibus**

---

## ✨ Features

### **1. Additional Python Packages**
The following Python packages are pre-installed using the method recommended in the Grist Help Center:

- `requests`
- `numpy`
- `beautifulsoup4`
- `jinja2`
- `pandas` (added 2023.10.7)
- `selenium` (added 2023.10.7)

If you need more Python packages included in the image, feel free to open an issue in this repository.

### **2. Multi-Architecture Support**
Both images are built for:

- `linux/amd64`
- `linux/arm64`

### **3. Automated Monthly Updates**
A GitHub Actions workflow:

- Builds the images based on the **latest official Grist images**
- Pushes updates **automatically every month**
- Can also be triggered **manually** at any time

Automated update schedule began on **2025-11-28**.

---

## 🚀 Build & Deployment

This repository uses GitHub Actions to:

1. Check out the source code  
2. Build Docker images using Docker Buildx  
3. Push images to Docker Hub  
4. Maintain multi-arch support  
5. Provide both automated and manual triggers  

No additional setup is required—Docker Hub will always contain the latest monthly build.

---

## 📦 Docker Hub

You can pull the images here:

- **Grist:** `docker pull kenny2023/grist:latest`
- **Grist Omnibus:** `docker pull kenny2023/grist-omnibus:latest`

---

## 📝 Changelog (Key Dates)

- **2023.10.07** — Added `pandas` and `selenium` packages  
- **2025.11.28** — Enabled automatic monthly builds via GitHub Actions  

---

## 🙏 Acknowledgments

Special thanks to:

- **ChatGPT** — for guidance on building and pushing multi-arch Docker images  
- **Grist** — for their excellent open-source product and documentation  

---

## 📄 License

This project follows the licensing terms of the original Grist images.  
Please refer to the respective upstream repositories for details.
