# Temet — Project Instructions & Workspace Guidelines

> *"Temet nosce" — Know thyself.*
> A hands-on exploration of language models and machine learning culminating in an interactive art installation making these concepts visible.

---

## 1. Project Overview & Objectives

- **Mission**: Demystify machine learning and LLM internals through practical experimentation, and translate core mechanisms (attention, representations, loss landscapes, emergent behaviors) into an engaging, interactive physical or digital art installation.
- **Key Themes**: Interpretability, self-reflection ("know thyself"), human-machine cognition, and interactive visualization.
- **Current Phase**: [ ] Foundational ML experiments / [ ] Model architecture / [ ] Interactive installation prototype / [ ] Exhibition build

---

## 2. Tech Stack & Environment (Customize as needed)

- **Language / Runtime**: Python 3.11+ / Node.js (or Web-based frontend)
- **ML / Deep Learning**: PyTorch / JAX / Hugging Face Transformers / tinygrad
- **Visualization & Creative Tech**: Three.js / WebGL / Canvas / TouchDesigner / p5.js / Streamlit
- **Package & Environment Management**: `uv` / `poetry` / `conda` / `pnpm`
- **Testing & Quality**: `pytest`, `ruff`, `mypy`

---

## 3. Project Structure (Proposed / Work-in-Progress)

```text
temet/
├── README.md           # Project introduction and conceptual background
├── GEMINI.md           # AI assistant guidelines and workspace rules (this file)
├── notebooks/          # Exploratory research, learning notes, and prototyping
├── src/                # Core implementation
│   ├── models/         # Neural network / LLM architectures from scratch
│   ├── training/       # Training loops, loss functions, tokenization
│   ├── viz/            # Visualization engines, attention maps, latent space maps
│   └── installation/   # Interactive runtime / sensor or interface connectors
├── web/                # Interactive web frontend / viewer (if applicable)
├── experiments/        # Experiment tracking, logs, checkpoints, configs
├── tests/              # Unit and integration tests
└── scripts/            # Automation, data ingestion, and run scripts
```

---

## 4. Common Commands & Workflows

Update these commands as tools and dependencies are configured:

### Environment Setup
```bash
# Python virtual environment (e.g., using uv or venv)
uv venv && source .venv/bin/activate
uv pip install -r requirements.txt
```

### Running Experiments & Training
```bash
python -m src.training.train --config configs/base.yaml
```

### Testing & Verification
```bash
# Run unit tests
pytest

# Code formatting and linting
ruff check .
ruff format .
```

### Interactive / Frontend Development
```bash
# Start local visualization server (if applicable)
npm run dev
```

---

## 5. Coding Standards & Conventions

- **Clarity & Educational Value**: Code should prioritize readability and conceptual clarity alongside performance. Comment key mathematical operations and tensor transformations (e.g., annotate tensor shapes like `[batch_size, seq_len, d_model]`).
- **Reproducibility**: Explicitly set random seeds in experiment scripts. Keep configurations decoupled from code (e.g., via YAML or dataclasses).
- **Type Annotations**: Use Python type hints (`typing` / `jaxtyping`) for public functions and tensor shapes where practical.
- **Minimal Dependencies**: Keep foundational implementations lean before introducing heavyweight libraries.

---

## 6. Guidelines for the AI Assistant

When working on this codebase:
- **Pedagogical & Intuitive**: Explain the "why" behind model mechanics and mathematical decisions when designing neural architectures.
- **Modular & Incremental**: Build components incrementally with accompanying unit tests or sanity checks (e.g., verifying forward pass shapes, gradient flow, loss convergence).
- **Artistic & Experiential Focus**: Keep the end goal in mind—translating internal representations and activations into tangible, aesthetic experiences for visitors.
- **Keep Documentation Updated**: Whenever new modules, workflows, or dependencies are introduced, update this file and `README.md`.
