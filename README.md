# Python Setup for Windows

Focuses on initializing projects from templates and managing tools with Poetry and Pipx.

## 1. Project Setup: GitHub Template

1. **Clone:** Create a new repo from your template on GitHub and clone it locally:
    ```cmd
    git clone [https://github.com/user/new-project.git](https://github.com/user/new-project.git)
    cd new-project
    ```
2. **Initialize Environment:** Set Python 3.13 and install dependencies from `pyproject.toml`:
    ```cmd
    poetry env use 3.13
    poetry install
    ```
3. **Hooks:** Activate pre-commit hooks:
    ```cmd
    pre-commit install
    ```

## 2. Maintenance Commands
| Task           | Command         |
|:---------------|:----------------|
| **Updates**    | `poetry update` |
| **Linting**    | `ruff check .`  |
| **Type Check** | `pyright`       |

## 3. Tool Management with Pipx
Pipx isolates CLI tools in private virtual environments to avoid global dependency conflicts.

### Key Commands:
* **Install:** `pipx install [tool]` (e.g., `ruff`)
* **Execute (Once):** `pipx run [tool]`
* **List/Upgrade:** `pipx list` or `pipx upgrade-all`

### Why Pipx?
Unlike `pip install --user`, Pipx keeps tools like Poetry or Ruff in hidden, independent environments, ensuring they don't break each other or your projects.