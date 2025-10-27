# 🤖 GitHub Profile README Auto-Update System

<div align="center">

<video src="https://raw.githubusercontent.com/noobhacker02/github-readme-automation/main/repo_automate.mp4" width="100%" autoplay loop muted playsinline>
  Your browser does not support the video tag.
</video>

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)




Automatically fetch and display your GitHub projects in your profile README.
<br>
<a href="#✨-features">Features</a> • <a href="#🚀-installation">Installation</a> • <a href="#🎨-customization">Customization</a> • <a href="#🛠️-manual-trigger">Manual Trigger</a>

</div>

---

## 🎯 Overview

This project automatically updates your GitHub profile README (e.g., `Your-Username/Your-Username`) with your latest projects based on repository topics/tags. It uses a GitHub Action to run a Python script daily, fetch your tagged projects, and commit the changes back to your README.

## ✨ Features

* **🔄 Automatic Daily Updates:** Runs on a schedule (e.g., every day at midnight UTC).
* **🏷️ Tag-Based Filtering:** Only displays repos with topics you define (e.g., `showcase`, `ai`, `rag`).
* **🎨 Custom Image Support:** Automatically finds and uses a custom preview image (e.g., `RepoName.png`) from your project, or falls back to the standard GitHub OpenGraph image.
* **📱 Mobile Responsive:** The generated HTML cards work perfectly on all devices.
* **⏰ Last Updated Timestamp:** Shows exactly when the project list was last refreshed.
* **🚀 Zero Maintenance:** Set it and forget it.

---

## 🖼️ Preview

Your profile README will automatically display clean, modern project cards like this:


*(Suggestion: Add a screenshot of your own profile's project section here)*

---

## 🚀 Installation

You can set this up in your own GitHub profile in 5 minutes.

### Step 1: Create the File Structure in Your Profile Repo

In your **profile repository** (the one named `Your-Username/Your-Username`), create the following folder and file structure:
