# Copilot Instructions

This workspace uses UV for Python package management and includes a Jupyter notebook for data analysis.

## Project Structure
- Python project with UV package manager
- Jupyter notebooks for interactive development
- Virtual environment managed by UV
- Data directories following industry best practices

## Development Guidelines
- Use UV commands for package management (`uv add`, `uv remove`, `uv sync`)
- Run notebooks interactively in VS Code
- Keep dependencies in `pyproject.toml`
- Store datasets in `data/raw/`, processed data in `data/processed/`

## Workspace Creation Prompt

To recreate this workspace structure using GitHub Copilot, use:

```
#create_new_workspace Python data analysis workspace with:
- UV package manager (Astral)
- Initialize with 'uv init' in current directory (use '.')
- Create virtual environment with 'uv venv'
- Install jupyter and ipykernel using 'uv add' (NOT 'uv pip')
- Create notebook.ipynb with welcome cells
- Install Python and Jupyter extensions
- Create data directories: data/raw/, data/processed/, data/external/
- Add data/.gitignore to exclude datasets from git
- Add data/README.md explaining directory structure and best practices
- Update main README.md with project structure and usage instructions
- Follow Python data science best practices for folder structure
```
