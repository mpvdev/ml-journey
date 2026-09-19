# Repository Guidelines

## Project Structure & Module Organization

This repository is a learning workspace for DeepLearning.AI's Machine Learning Specialization, organized by course and week:

```text
Courses/<course>/<weeks>/<week>/
```

The numbered course directories follow the specialization sequence, and each course is divided into weeks. The current material is in `Courses/01/Weeks/01/`, corresponding to the opening supervised-learning material. Jupyter notebooks (`.ipynb`) contain the lesson explanations, exercises, code, and outputs. Supporting datasets belong in `data/`; for example, `data/pokemon.csv` is the reusable Pokémon dataset. Supporting visualization settings belong beside the notebook; for example, `deeplearning.mplstyle` is loaded by the Model Representation lab. There is currently no separate application source tree, test suite, or asset directory.

## Build, Test, and Development Commands

There is no project-wide build system or automated test command. Work with notebooks using Jupyter:

```bash
jupyter notebook
# or
jupyter lab
```

Open the relevant notebook from `Courses/`, run its cells from top to bottom, and confirm that plots render and outputs are reproducible. Run Jupyter with the notebook's directory as the working directory so relative paths resolve correctly, for example `cd Courses/01/Weeks/01 && jupyter lab`.

## Coding Style & Naming Conventions

Use Python conventions consistent with the existing notebooks: four-space indentation, `snake_case` for variables and functions, and concise comments that explain instructional intent. Keep imports near the top of a code cell and group scientific imports clearly (for example, NumPy, pandas, and Matplotlib). Use Markdown headings to structure lessons and LaTeX for mathematical notation. Name notebooks and supporting files descriptively, using the existing title-style notebook pattern and lowercase names for reusable support files. Every imported course lab should have a clearly labeled parallel Pokémon example using `data/pokemon.csv` when the concept supports one. Keep the original course file unchanged; create a companion file beside it, using a suffix such as `- Pokemon`.

## Testing Guidelines

No formal testing framework or coverage requirement is configured. Treat a complete top-to-bottom notebook execution as the primary validation: restart the kernel, run all cells, inspect outputs, and verify that referenced local files exist. Avoid committing stale, excessive, or machine-specific outputs unless they are useful to the lesson.

## Commit & Pull Request Guidelines

Existing commits use short, imperative descriptions such as `completed the first lab` and `first commit`. Follow the same concise style, while making the change clear (for example, `add linear regression exercise`). Pull requests should describe the course/week affected, summarize notebook or documentation changes, mention validation performed, and include screenshots when a rendered plot or layout change is relevant.

## Repository Hygiene

Preserve the course hierarchy and nearby supporting files. Do not commit virtual environments, notebook checkpoints, editor metadata, credentials, or generated files unrelated to the lesson.
