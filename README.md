# Python UV Workspace with Jupyter Notebook

A Python development environment using [UV](https://github.com/astral-sh/uv) for fast, reliable package management with an integrated Jupyter notebook.

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

## Getting Started

### Prerequisites

- Python 3.13.7 (or compatible version)
- UV package manager installed

### Setup

The environment is already set up with:
- Virtual environment created in `.venv/`
- Jupyter and IPython kernel installed
- VS Code Python and Jupyter extensions configured

### Using the Notebook

1. Open `notebook.ipynb` in VS Code
2. Select the Python kernel from `.venv/`
3. Place your datasets in `data/raw/`
4. Start coding and running cells interactively

### Working with Data

Place your datasets in the appropriate directory:
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
