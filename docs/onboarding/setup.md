# Setup

We have 2 different methods of developing the code for this project

## Method 1: Repo level development

We use **GitHub Codespaces** to maintain a consistent development environment across the team. Docker handles all dependency installation automatically (it runs in the browser)

### If you have collaborator access

1. Navigate to the repository on GitHub.
2. Click the green **`<> Code`** button.
3. Select the **Codespaces** tab.
4. Click **Create codespace on main** (or the branch you want to work from).
5. Wait for the container to build (Give it a good 10-15 minutes).
6. Once the Codespace is ready, you'll have a full VS Code editor in your browser with all dependencies pre-installed.
7. Make your changes, then commit and push to a branch (or directly to `main` if permitted).

### If you don't have collaborator access (fork-based workflow)

1. **Fork** the repository by clicking **Fork** in the top-right of the repo page.
2. Open your fork, click **`<> Code` -> Codespaces -> Create codespace on main**.
3. Work on your changes in the Codespace as usual.
4. Commit and push your changes to your fork.
5. Go to GitHub and open a **Pull Request** from your fork's branch into the original repository's `main` branch.

### Tips

- **Saving work:** Changes are auto-saved, but remember to commit and push before closing the Codespace.
- **Stopping a Codespace:** You can stop a Codespace to save compute time (your work is preserved and you can resume later) Go to **Code -> Codespaces -> the `...` menu -> Stop codespace**.
- **Resuming:** Reopen a Codespace anytime from the same **Codespaces** tab.
- **Idle timeout:** Codespaces automatically stop after a period of inactivity (default 30 minutes), but your data is retained.

## Method 2: Notebook level development

For the ML workflow, we prefer **Jupyter notebooks** (`.ipynb` files) since they are standalone scripts that can be run on cloud providers with GPU access, such as **Google Colab**.

### Quick Start

1. Go to [Google Colab](https://colab.research.google.com/) (sign in with a Google account).
2. Click **Upload** from the landing page (or **File -> Upload notebook**).
3. Select the `.ipynb` file from your computer and upload it.
4. Once loaded, change the runtime type to use a GPU:
   - Click **Runtime -> Change runtime type**.
   - Under **Hardware accelerator**, select **T4 GPU**.
   - Click **Save**.
5. Run cells by clicking the ▶️ button (or `Shift + Enter`).
6. Go ham.

### Tips

- **Saving changes:** Click **File -> Save** or **File -> Save a copy in Drive** to keep your work. Uploaded notebooks are not automatically persisted. unsaved changes will be lost if you close the tab.
- **Downloading:** Use **File -> Download -> Download .ipynb** to export the notebook back to your computer.
- **Session limits:** Free-tier Colab sessions have idle and maximum runtime limits. If your session disconnects, just reconnect and re-run your cells.
- **File uploads from your computer:** Use the folder icon on the left sidebar to upload data files to the Colab runtime environment. Note: these are temporary and cleared when the session ends.
- **Clone a repo directly:** You can also pull a notebook straight from GitHub. Go to **File -> Open notebook -> GitHub**, paste the repo URL, and select the `.ipynb` file you want.