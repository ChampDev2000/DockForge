
# 🚀 DevEnvWorks

### *Ready-to-use Dockerized development environments for any stack, tool, or purpose.*

---

## 🧠 Overview

**DevEnvWorks** is a collection of **preconfigured Docker development environments** designed to make setup simple and coding faster.
Whether you’re working on **AI/ML**, **Web Development**, **CI/CD**, or **Security Tools**, just pull an environment, run a single command, and start building, no manual installations, no dependency issues.

Each environment comes with **optimized Dockerfiles**, **sample configurations**, and **ready-to-run containers**.

---

## 🧰 What’s Inside

| Category             | Environment                                | Description                                                                          |
| -------------------- | ------------------------------------------ | ------------------------------------------------------------------------------------ |
| Development Tools | `dev-tools-env`                            | Includes Git, VS Code Server, build tools, compilers, and debugging utilities.       |
| Web Stacks        | `mern-env`, `django-env`, `rails-env`      | Preconfigured environments for popular web frameworks.                               |
| AI/ML             | `cv-env`, `aiml-env`                       | Ready-to-train ML environments with Python, PyTorch/TensorFlow, OpenCV, and Jupyter. |
| Security          | `nmap-env`, `ctf-env`                      | Security analysis and Capture-The-Flag challenge setups.                             |
| CI/CD             | `jenkins-env`, `gitlab-ci-env`             | Environments to test continuous integration/deployment pipelines.                    |
| Database Systems | `mysql-env`, `postgres-env`, `mongodb-env` | Containers for databases, preconfigured with sample schemas.                         |

> 💡 Each folder contains its own `Dockerfile`, `README.md`, and usage instructions.

---

## 🐳 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/<your-username>/DevEnvWorks.git
cd DevEnvWorks
```

### 2️⃣ Choose your environment

Navigate to the environment folder you want to use.
For example:

```bash
cd web-stacks/mern-env
```

### 3️⃣ Build and run

```bash
docker build -t mern-dev .
docker run -it -p 3000:3000 mern-dev
```

That’s it! You’re inside a ready-to-code development container. 🎉

---

## 🧑‍💻 Folder Structure

```
DevEnvWorks/
├── ai-ml/
│   ├── cv-env/
│   ├── aiml-env/
├── web-stacks/
│   ├── mern-env/
│   ├── django-env/
│   └── rails-env/
├── ci-cd/
│   ├── jenkins-env/
│   └── gitlab-ci-env/
├── databases/
│   ├── mysql-env/
│   ├── postgres-env/
│   └── mongodb-env/
├── dev-tools/
│   └── base-dev-env/
└── README.md
```

---

## 🧩 How to Contribute

We welcome community contributions!
Here’s how you can help:

1. Pick or propose a new environment (e.g., `springboot-env`, `nextjs-env`, `kali-env`).
2. Create a folder with a clear Dockerfile and minimal setup.
3. Add usage instructions in a local `README.md`.
4. Submit a pull request with a short description.

> Make sure your environment follows the **standard naming**, **lightweight base image**, and **non-root user** practices.

---

## 📦 Naming Convention

| Type               | Example       | Base Image               |
| ------------------ | ------------- | ------------------------ |
| Language/Framework | `mern-env`    | `node:20-alpine`         |
| Tool               | `jenkins-env` | `jenkins/jenkins:lts`    |
| AI/ML              | `cv-env`      | `python:3.10`            |
| Security           | `ctf-env`     | `kalilinux/kali-rolling` |

---

## 🧱 Why Use This?

✅ Zero setup, ready in seconds \
✅ Reproducible environments across systems \
✅ Easy to switch stacks without reconfiguring your host machine \
✅ Great for classrooms, hackathons, and quick experiments \
✅ Extensible and community-driven

---

## 🗺️ Roadmap

* [ ] Add environments for **Rust**, **Go**, and **Spring Boot**
* [ ] Add support for **Dev Containers (VS Code)**
* [ ] Publish images to **Docker Hub**
* [ ] Provide **compose.yaml** for multi-service stacks
* [ ] Add **benchmark and size optimization** badges

---

## 📜 License

This repository is licensed under the **MIT License**, feel free to use, modify, and share!

---

## 🌟 Star This Repository

If this project helps you save time or inspires your workflow 
⭐ **Star it on GitHub** to support ongoing development!

---

**Built with ❤️ by Developers, for Developers.**
