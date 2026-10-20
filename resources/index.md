---
layout: default
title: Practical Lab / Resources
nav_order: 5
permalink: /resources/
description: "Practical laboratory guides, development environment setups, Git instructions, and academic reference resources for Year Two Computer Science at the University of Makeni."
---

# Practical Lab & Academic Resources
{: .fs-9 }

Department of Computer Science &bull; University of Makeni
{: .fs-5 .text-delta .text-muted }

---

This portal contains development environment setup instructions, lab policy guidelines, open-source software distributions, and academic reference materials required for Year Two coursework.

## Table of Contents
- [Java Development Environment Setup](#java-setup)
- [Git & Version Control Workflow](#git-setup)
- [Database & SQL Tools Setup](#database-setup)
- [University ICT Lab Guidelines](#lab-guidelines)
- [Student Academic Developer Packs](#student-packs)

---

## Java Development Environment Setup
{: #java-setup }

All Year Two programming in **CS211 (OOP)** and **CS212 (Data Structures)** requires a verified installation of **Java Development Kit (JDK) 21 LTS**.

### 1. Installing Java JDK 21 (LTS)
- **Windows:** Download the x64 Installer from [Adoptium Eclipse Temurin 21](https://adoptium.net/temurin/releases/?version=21) or [Oracle JDK 21](https://www.oracle.com/java/technologies/downloads/#java21). During setup, ensure **"Add to PATH"** and **"Set JAVA_HOME"** are checked.
- **macOS (Homebrew):**
  ```bash
  brew install openjdk@21
  ```
- **Linux (Ubuntu/Debian):**
  ```bash
  sudo apt update
  sudo apt install openjdk-21-jdk
  ```

Verify your installation in your terminal:
```bash
java --version
javac --version
```

### 2. Recommended Integrated Development Environments (IDEs)
- **Visual Studio Code:** Lightweight, fast, and highly extensible. Install the official **Extension Pack for Java** by Microsoft.
- **IntelliJ IDEA Community Edition:** Free, feature-rich Java IDE tailored for enterprise OOP development.

---

## Git & Version Control Workflow
{: #git-setup }

All collaborative software engineering projects in **CS215** must be tracked and submitted using Git.

### Basic Setup
Configure your username and official student email:
```bash
git config --global user.name "Your Full Name"
git config --global user.email "your.student.id@unimak.edu.sl"
```

### Recommended Workflow
1. **Clone the project repository:**
   ```bash
   git clone <repository-url>
   ```
2. **Create a feature branch:**
   ```bash
   git checkout -b feature/module-implementation
   ```
3. **Commit your changes with descriptive messages:**
   ```bash
   git add .
   git commit -m "feat(cs211): implement StudentRecord class and unit tests"
   ```
4. **Push branch and open a Pull Request:**
   ```bash
   git push origin feature/module-implementation
   ```

---

## Database & SQL Tools Setup
{: #database-setup }

For **CS213 (Database Management Systems)**, students will practice schema creation, normalization, and complex querying on relational engines.

- **MySQL Community Server 8.0:** The primary relational database used in practical lab sessions.
- **DBeaver Universal Database Tool:** A free multi-platform database administration tool supporting MySQL, PostgreSQL, and SQLite.
- **Alternative:** [PostgreSQL](https://www.postgresql.org/download/) for advanced SQL standard compliance.

---

## University ICT Lab Guidelines
{: #lab-guidelines }

The Department of Computer Science maintains dedicated computer laboratories (Main ICT Lab, ICT Lab 1, and ICT Lab 2) for scheduled sessions:

1. **Access:** Lab entry is strictly reserved for students with valid University of Makeni student identification cards during scheduled timetable hours.
2. **Hardware Care:** Do not unplug, alter, or relocate lab desktop terminals or network cables.
3. **Personal Laptops:** Students are encouraged to bring personal laptops configured with the required development toolchains. Surge protectors and power outlets are available at all student benches.
4. **Data Hygiene:** Public lab machines are refreshed periodically. Always push your project work to GitHub or store backups on your personal USB flash drive.

---

## Student Academic Developer Packs
{: #student-packs }

All enrolled Computer Science students at the University of Makeni qualify for free professional developer tooling:

- **GitHub Student Developer Pack:** Free GitHub Pro, free private repositories, Copilot access, and cloud credits on DigitalOcean, Microsoft Azure, and AWS Educate. [Apply on GitHub Education](https://education.github.com/pack).
- **JetBrains Educational License:** Free access to IntelliJ IDEA Ultimate, WebStorm, PyCharm Professional, and DataGrip. [Register with your university email](https://www.jetbrains.com/community/education/#students).
