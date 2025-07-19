# Prompt Engineering and Project Engagement Analysis

A research project analyzing correlations between prompt engineering practices and repository engagement metrics in LLM-integrated open-source projects.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Research Question

Do prompt characteristics (type, complexity, reuse patterns) correlate with project engagement indicators (stars, forks, contributor activity) in LLM-integrated repositories?

## What This Project Does

1. **Discovers LLM Repositories**: Uses GitHub Search API to identify repositories with LLM/prompt engineering patterns
2. **Extracts Metadata**: Collects engagement metrics, temporal data, and project characteristics
3. **Analyzes Relationships**: Tests correlations between prompt sophistication and community engagement


## Quick Start

### Prerequisites
- Python 3.8+
- GitHub API token (optional, for higher rate limits)

### Installation
```bash
# Clone the repository
git clone https://github.com/n4m3name/SENG404-Project.git
cd SENG404-Project

# Install dependencies
pip install pandas matplotlib seaborn jupyter requests python-dotenv

# Set up environment (optional)
echo "GITHUB_TOKEN=your_token_here" > .env
```

### Run Analysis
```bash
# Start Jupyter and open the data collection notebook
jupyter notebook src/data_sourcing.ipynb

# Or run pilot analysis
jupyter notebook src/pilot.qmd
```

## Repository Structure

```
├── data/                           # Generated datasets
│   ├── matched_repositories.csv    # Repositories with LLM keywords
│   ├── repo_metadata.csv          # GitHub metadata
│   └── combined_repository_data.csv # Merged analysis dataset
├── src/                           # Source code
│   ├── data_sourcing.ipynb        # Data collection pipeline
│   └── pilot.qmd                  # Pilot analysis and validation
├── paper/                         # Research documentation
│   └── proposal/                  # Project proposal
└── README.md                      # This file
```

## How It Works

1. **Repository Discovery**: Searches GitHub for 30+ LLM-related keywords
2. **Data Collection**: Extracts repository metadata via GitHub API
3. **Analysis**: Correlates LLM integration signals with engagement metrics
4. **Visualization**: Generates plots showing relationships and trends

### Keywords Searched
- **APIs**: `openai.ChatCompletion.create`, `PromptTemplate`, `RetrievalQA`
- **Patterns**: `"prompt = "`, `"system": "`
- **Frameworks**: `llama_cpp`, `AutoGPT`, `FAISS`, `transformers.pipeline`

## Current Status

- Data collection pipeline implemented
- Pilot analysis completed
- Prompt extraction in development
- Statistical modeling planned

## Contributing

This is an academic research project. If you're interested in:
- **Reproducing results**: All code and data are included
- **Extending analysis**: Fork and submit PRs
- **Using the dataset**: See `data/` directory

## Citation

```bibtex
@misc{strasdin2025prompt,
  title={Prompt Engineering and Project Engagement in LLM-Enabled Repositories},
  author={Strasdin, Evan},
  year={2025},
  school={University of Victoria},
  note={SENG-404 Software Engineering Research Project}
}
```

## Limitations

- Limited to Python repositories on GitHub
- Keyword-based detection may miss some LLM usage
- Engagement metrics are proxies for actual project quality
- Rate-limited by GitHub API

## Contact

**[Evan Strasdin](mailto:evn.strsdn@pm.me)**
University of Victoria - SENG-404

---

*Part of ongoing research into prompt engineering as a software development practice*