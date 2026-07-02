# 🐍 Modern Python Development Environment (uv)

[![Python](https://img.shields.io/badge/Python-3.13-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-2E7D32)](LICENSE)
[![Linting](https://img.shields.io/badge/Linting-Ruff-8B0000?logo=ruff&logoColor=white)](https://docs.astral.sh/ruff/)
[![Static Typing](https://img.shields.io/badge/Static%20Typing-Pyright-4B32C3?logo=microsoft&logoColor=white)](https://github.com/microsoft/pyright)
[![Dependency Management](https://img.shields.io/badge/Dependency%20Management-uv-FF7A00?logo=rust&logoColor=white)](https://docs.astral.sh/uv/)
[![CI](https://github.com/miguelcosta2c/modern-python-development-environment/actions/workflows/ci.yml/badge.svg)](https://github.com/miguelcosta2c/modern-python-development-environment/actions/workflows/ci.yml)

A **modern Python development template** powered by **uv**, following current best practices such as:

- `src/` layout
- Static typing with **Pyright**
- Linting and formatting with **Ruff**
- Testing with **Pytest**
- CLI scripts via `pyproject.toml`
- Environment variable support with **python-dotenv**

Ideal for quickly starting professional and maintainable Python projects.

---

## 🚀 Tech Stack

- **Python 3.13**
- **uv** – dependency and virtual environment manager
- **Ruff** – linter and code formatter
- **Pyright** – static type checker
- **Pytest** – testing framework
- **python-dotenv** – environment variable management

---

## 📂 Project Structure

```text
.
├── .vscode/                 # VS Code configuration
│   ├── extensions.json
│   └── settings.json
├── src/
│   ├── my_package/
│   │   ├── __init__.py
│   │   ├── my_module.py     # Core logic
│   └── main.py              # Entry point
├── tests/
│   └── test_smoke.py
├── .env                     # Environment variables
├── .gitignore               #
├── .python-version          # Python version (3.13.11)
├── pyproject.toml           # Project configuration
├── requirements.txt         # Dependencies (compatibility)
├── uv.lock                  # uv lockfile
└── README.md
```

---

## ⚙️ Requirements

- **Python 3.13+**
- **uv** installed

Install `uv`:

```bash
pip install uv
```

Or (recommended):

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/miguelcosta2c/modern-python-development-environment
cd modern-python-development-environment
```

Create the virtual environment and install dependencies:

```bash
uv sync
```

Install development dependencies:

```bash
uv sync --group dev
```

---

## ▶️ Running the Project

### Run with Python

```bash
python src/my_package/main.py
```

### Run as a CLI command

The project defines a console script in `pyproject.toml`:

```toml
[project.scripts]
project-cli = "my_package.my_module:run_from_script"
```

After installing the project in the environment:

```bash
uv run project-cli
```

---

## 🧪 Testing

Run tests with:

```bash
uv run pytest
```

---

## 🧹 Linting & Formatting (Ruff)

Check for issues:

```bash
uv run ruff check .
```

Automatically fix issues:

```bash
uv run ruff check . --fix
```

Format the code:

```bash
uv run ruff format .
```

---

## 🧠 Static Type Checking (Pyright)

```bash
uv run pyright
```

Configured in **strict mode** for maximum type safety.

---

## 🌱 Environment Variables

This project uses **python-dotenv**.

Create a `.env` file or rename the `.env.example` file:

```env
EXAMPLE_VAR=hello_world
```

Load it in your application when needed.

---

## 📌 Best Practices Included

- `src/` layout (recommended by the Python Packaging Authority)
- Centralized configuration via `pyproject.toml`
- Reproducible environments with `uv.lock`
- Clear separation between production and development dependencies

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👤 Author

**Miguel Costa**
📧 [miguelcosmecosta@gmail.com](mailto:miguelcosmecosta@gmail.com)

---

## ⭐ Tip

If you find this template useful, consider giving the repository a ⭐!
