# WORKFLOW GUIDE

For details, see <https://github.com/denisecase/pro-analytics-01>

## 01 Set Up Machine
For details, see <https://github.com/denisecase/pro-analytics-01>

Perform or verify **one-time tasks** including:
1. View file extensions and hidden files and folders.
2. Install (or verify) a package manager for your operating system.
3. Install Python, Git, and Visual Studio (VS) Code for your operating system.
4. Configure Git
5. Install common VS Code extensions. **IMPORTANT** (see [link](https://github.com/denisecase/pro-analytics-01/blob/main/01-machine-setup/05-install-vscode-extensions.md))
6. Create a Projects folder to hold your projects. 
7. Create a GitHub account.

---  
## 02-Project-Initialization
For details, see <https://github.com/denisecase/pro-analytics-01>

Follow the steps to start a new project by either:
1. Copy an existing project OR start a new project from scratch.
2. Clone your new GitHub repo to your machine. 
3. Add common files such as .gitignore and requirements.txt.
4. Git add-commit-push the changes to GitHub.
5. Create a local project virtual environment for Python.

I always start in GitHub with a README or existing project, then clone down my GitHub repo to my machine. 
On my machine, in VS Code, I add .gitignore and requirements.txt from the pro-analytics-01 repository linked above. 
After adding the two files, I git add-commit-push and create my local project virtual environment. 
On Windows, my commands were:

```powershell
git add . 
git commit -m "add .gitignore and req.txt"
git push -u origin main
py -m venv .venv
```
---
## 03-Repeatable-Workflow
For details, see <https://github.com/denisecase/pro-analytics-01>

Follow the **repeatable steps** for working on Python projects. 
These steps are typically followed whenever we make changes to a project. The workflow includes:
1. Pull any recent changes from GitHub.
2. Activate the virtual environment.
3. Install dependencies.
4. Run scripts and/or Jupyter notebooks.
5. Make updates, verify the code still runs, and git add-commit-push to GitHub. 

Important: Use 2-step installation (scikit-learn is BIG)

- First, install from requirements.txt with scikit-learn commented out.
- Second, uncomment scikit-learn in requirements.txt and rerun the install command.
- It works better in two parts. 

On Windows, before starting work on my machine:

```shell
git pull
```

On Windows, activate and install into .venv:

```shell
.\.venv\Scripts\activate
py -m pip install --upgrade pip setuptools wheel
py -m pip install -r requirements.txt
py -m pip install -r requirements.txt
```

After useful work
```shell
git add . 
git commit -m "add .gitignore and req.txt"
git push -u origin main
```
---
## Jupyter Notebook Kernel

To select notebook kernel, in VS Code use:

- View / Command Palette... (CTRL SHIFT P)
- Type: Python: Select Interpreter 
- Choose your .venv from the list

## IMPORTANT: If `.venv` packages (e.g., `pandas`) are not recognized  

1. Create a `.vscode` folder in your project.  
2. Add a `settings.json` file.  
3. Copy the full content from our shared [`.vscode/settings.json`](./.vscode/settings.json).  
4. Close and reopen your notebook.  
5. Activate the `.venv` environment.  
6. Verify or set the kernel as needed.  
