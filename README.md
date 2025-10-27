
# 🤖 GitHub Profile README Auto-Update System

<div align="center">

<img src="https://github.com/noobhacker02/github-readme-automation/blob/main/repo_automate.gif" alt="Git Reader Header Banner" width="100%">

<br>

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

<br>

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

## 🚀 Installation

You can set this up in your own GitHub profile in 5 minutes.

### Step 1: Create the File Structure in Your Profile Repo

In your **profile repository** (the one named `Your-Username/Your-Username`), create the following folder and file structure:

```

Your-Username/
├── .github/
│   └── workflows/
│       └── update-readme.yml  
├── scripts/
│   └── update\_projects.py  
├── requirements.txt  
└── README.md

````

### Step 2: Add Project Markers to your `README.md`

In your `README.md` file, add these two HTML comments. The script will find these tags and replace everything between them.

```markdown

<!--START_PROJECTS_LIST-->
<!--END_PROJECTS_LIST-->
````

### Step 3: Add the Code Files

Copy the code from this repository into the files you just created:

  * **`.github/workflows/update-readme.yml`:** [Copy the workflow code from this repo](https://www.google.com/search?q=link-to-your-workflow-file)
  * **`scripts/update_projects.py`:** [Copy the Python script from this repo](https://www.google.com/search?q=link-to-your-script-file)
  * **`requirements.txt`:**
    ```
    requests==2.31.0
    ```

### Step 4: Configure GitHub Actions Permissions

You must give the GitHub Action permission to write to your repository.

1.  Go to your profile repository's **Settings** tab.
2.  Navigate to **Actions** \> **General**.
3.  Scroll down to **"Workflow permissions"**.
4.  Select **"Read and write permissions"**.
5.  Click **Save**.

### Step 5: Tag Your Repositories

For any project you want to appear on your README:

1.  Go to that project's repository page.
2.  Click the **⚙️ (gear icon)** next to the "About" section.
3.  In the "Topics" field, add one of the tags you defined in the script (e.g., `showcase`, `ai`).
4.  Click **"Save changes"**.

That's it\! Your README will update on the next scheduled run or when you trigger it manually.

-----

## 🛠️ Manual Trigger

You don't have to wait for the daily schedule to see your changes.

1.  Go to your profile repository's **Actions** tab.
2.  On the left, click **"Update README with Projects"**.
3.  Click the **"Run workflow"** button on the right.

-----

## 🎨 Customization

### Change Target Tags

Edit `scripts/update_projects.py` to add or remove your desired tags:

```python
TARGET_TAGS = ["rag", "lln", "showcase", "ai", "your-custom-tag"]
```

### Change Update Frequency

Edit `.github/workflows/update-readme.yml` and change the `cron` schedule:

```yaml
schedule:
  # - cron: '0 0 * * *'  # Daily at midnight (Default)
  - cron: '0 */6 * * *'  # Every 6 hours
  # - cron: '0 0 * * 1'    # Every Monday
```

### Add Custom Preview Images

For any project, you can add a custom image.

1.  Create a preview image for your project (e.g., `My-Awesome-Project.png`).
2.  The image name **must exactly match** your repository name.
3.  Push this image to the `main` branch of *that project's* repository.

The script will automatically find it and use it instead of the default GitHub preview.

-----

## 📜 License

This project is licensed under the MIT License - see the `LICENSE` file for details.

```
MIT LICENSE
```
