# Propose, Test, Reject

An LLM-agent framework for falsifiable hypothesis testing on the undeciphered Indus script.

LLM agents propose structural hypotheses about Indus signs (positional markers, numerals,
allographs, segmentation). A statistical verifier, which uses no LLM, accepts or rejects each
hypothesis on held-out data against null models. The framework is validated first on deciphered
scripts with their answers masked. **This project does not claim a decipherment.**

M.Tech (Computer Engineering) research project, 2026.

## Project layout

```
data/raw/          corpus files as received (not committed, see data/README.md)
data/processed/    cleaned, machine-readable corpus (not committed)
docs/              proposal, paper notes, research log
notebooks/         exploratory analysis
results/           figures and tables for the paper
src/indus/         library code (loader, statistics, verifier, agents)
tests/             unit tests
```

## Setup

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
pytest
```

## Data

The Indus corpus is used under research access and is **not** redistributed in this repository.
See [data/README.md](data/README.md).

## License

Code is released under the MIT License. Corpus data remains under its original terms.
