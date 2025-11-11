# Python UV Workspace with Jupyter Notebook

A Python development environment using [UV](https://github.com/astral-sh/uv) for fast, reliable package management with an integrated Jupyter notebook.

## Quick Start Guide

### Option 1: Clone This Repository (Recommended)

If you're setting up this workspace on a new PC:

1. **Clone the repository**
   ```powershell
   git clone https://github.com/untype/py-uv-jupnb-starter.git
   cd py-uv-jupnb-starter
   ```

2. **Install UV** (if not already installed)
   ```powershell
   # Windows PowerShell
   irm https://astral.sh/uv/install.ps1 | iex
   ```

3. **Create virtual environment**
   ```powershell
   uv venv
   ```

4. **Install dependencies**
   ```powershell
   uv sync
   ```

5. **Open in VS Code**
   ```powershell
   code .
   ```

6. **Select Python interpreter**
   - Press `Ctrl+Shift+P`
   - Type "Python: Select Interpreter"
   - Choose the interpreter from `.venv`

7. **Start working!**
   - Open `notebook.ipynb`
   - Place your datasets in `data/raw/`
   - Begin your analysis

### Option 2: Create New Project from Scratch

To create a brand new project based on this template:

1. **Create and navigate to your project directory**
   ```powershell
   mkdir my-analysis-project
   cd my-analysis-project
   ```

2. **Initialize UV project**
   ```powershell
   uv init --name my-analysis-project .
   ```

3. **Create virtual environment**
   ```powershell
   uv venv
   ```

4. **Install Jupyter dependencies**
   ```powershell
   uv add jupyter ipykernel
   ```

5. **Create data directories**
   ```powershell
   mkdir -p data/raw, data/processed, data/external
   ```

6. **Initialize git repository**
   ```powershell
   git init
   git add .
   git commit -m "Initial commit: Setup Python UV Jupyter workspace"
   ```

7. **Create GitHub repository** (choose one method):
   
   **Method A: Using GitHub CLI**
   ```powershell
   gh repo create my-analysis-project --public --source=. --remote=origin --push
   ```
   
   **Method B: Using VS Code**
   - Press `Ctrl+Shift+P`
   - Type "Publish to GitHub"
   - Follow the prompts
   
   **Method C: Manual GitHub setup**
   - Go to https://github.com/new
   - Create repository named `my-analysis-project`
   - Don't initialize with README
   - Then run:
     ```powershell
     git remote add origin https://github.com/YOUR_USERNAME/my-analysis-project.git
     git branch -M main
     git push -u origin main
     ```

## Project Structure

```
.
├── .github/
│   └── copilot-instructions.md  # GitHub Copilot workspace instructions
├── data/                         # Data directory (see data/README.md)
│   ├── raw/                      # Original, immutable datasets
│   ├── processed/                # Cleaned and transformed data
│   └── external/                 # Third-party data sources
├── .venv/                        # Virtual environment (managed by UV)
├── hello.py                      # Sample Python script
├── notebook.ipynb                # Jupyter notebook for interactive development
├── pyproject.toml                # Project configuration and dependencies
└── README.md                     # This file
```

## Working with the Environment

### Using the Notebook

1. Open `notebook.ipynb` in VS Code
2. Select the Python kernel from `.venv/` (if not already selected)
3. Place your datasets in `data/raw/`
4. Start coding and running cells interactively

### Managing Data
- **Original data** → `data/raw/` (never modify these files)
- **Cleaned data** → `data/processed/`
- **External data** → `data/external/`

See `data/README.md` for detailed guidelines.

### Managing Dependencies

Use UV commands to manage packages:

```powershell
# Add a new package
uv add <package-name>

# Remove a package
uv remove <package-name>

# Sync dependencies
uv sync

# Run Python scripts
uv run python hello.py
```

## Features

- **Fast Package Management**: UV provides pip-compatible package installation with significantly faster performance
- **Jupyter Integration**: Interactive notebook development with full VS Code support
- **Isolated Environment**: Virtual environment keeps dependencies project-specific
- **Modern Tooling**: Uses `pyproject.toml` for configuration following modern Python standards

## Next Steps

- Open `notebook.ipynb` to start exploring
- Add your project dependencies using `uv add`
- Configure additional settings in `pyproject.toml` as needed
