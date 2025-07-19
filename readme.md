# SENG-404 Project: Prompt Engineering and Project Engagement in LLM-Enabled Repositories

**Author**: Evan Strasdin
**Course**: SENG-404 Software Engineering Research  
**Git Repository**: [https://github.com/n4m3name/SENG404-Project](https://github.com/n4m3name/SENG404-Project)

## Project Overview

This research project investigates whether prompt characteristics—such as type, complexity, reuse patterns, and collaborative authorship—correlate with indicators of project activity and engagement in open-source LLM-integrated repositories. 

The study combines prompt classification with software repository mining to uncover whether observable prompt engineering patterns relate to collaboration and development dynamics in real-world LLM-integrated projects.

## Research Question

**Do prompt characteristics, such as type, complexity, reuse, and collaborative authorship, correlate with indicators of project activity and engagement in open-source LLM-integrated repositories?**

We analyze prompt artifacts extracted from public repositories using classification by prompt type and metric-based evaluation (prompt length, contributor interaction), comparing these features against repository-level signals including contributor count, issue resolution rate, and project growth over time.

## Motivation

Large Language Models (LLMs) like GPT-4 are now central to many software systems, with open-source tools such as LangChain, AutoGPT, and llama.cpp enabling developers to build entire applications around model behavior. In these systems, prompts function as logic, guiding how models reason, respond, and perform tasks, making prompt engineering a core software development activity.

While recent research has introduced prompt taxonomies and quality metrics, it remains unclear whether prompt characteristics are associated with broader indicators of project activity and engagement. This study addresses that gap through empirical analysis of real-world repositories.

## Methodology

### Data Collection Pipeline
1. **Repository Discovery**: Used GitHub Search API with 30+ LLM-related keywords to identify relevant repositories
2. **Metadata Extraction**: Collected engagement metrics (stars, forks, watchers), temporal data, and project characteristics  
3. **Prompt Extraction**: Extract actual prompt strings using static code parsing, regex, and heuristics
4. **Classification**: Categorize prompts by type (zero-shot, few-shot, chain-of-thought) and structural features
5. **Analysis**: Test correlations between prompt characteristics and engagement metrics

### Keywords Used
- API calls: `openai.ChatCompletion.create`, `PromptTemplate`, `RetrievalQA`
- Patterns: `"prompt = "`, `"system": "`
- Frameworks: `llama_cpp`, `AutoGPT`, `FAISS`, `transformers.pipeline`

## Project Structure

```
├── data/                           # Dataset files
│   ├── matched_repositories.csv    # Repositories matched by LLM keywords
│   ├── repo_metadata.csv          # GitHub repository metadata
│   └── combined_repository_data.csv # Merged analysis dataset
├── src/                           # Source code and analysis
│   ├── data_sourcing.ipynb        # Data collection pipeline
│   └── pilot.qmd                  # Pilot experiments and validation
├── paper/                         # Project documentation
│   └── proposal/                  # Proposal materials
└── Project files...
```

## Key Findings (Pilot Analysis)

✅ **Data Validation Complete**
- Successfully identified hundreds of LLM-integrated repositories
- Keyword matches range from 1-7+ per repository, indicating varying integration levels
- Clear variation in engagement metrics enables comparative analysis

📊 **Preliminary Results**
- Weak positive correlation (r ≈ 0.07) between keyword count and engagement
- Temporal surge in LLM repositories during 2023-2024 period
- Certain keywords (`"prompt="`, `ChatOpenAI`, `PromptTemplate`) more frequent in high-engagement repos

## Timeline & Status

- **✅ July 17-21**: Data cleaning and validation 
- **✅ July 17-24**: Pilot analysis and writeup
- **🔄 July 22-Aug 1**: Interim report (in progress)
- **📅 July 25-Aug 5**: Prompt extraction implementation
- **📅 Aug 1-10**: Prompt classification and feature engineering
- **📅 Aug 6-15**: Engagement modeling and statistical analysis
- **📅 Aug 10-23**: Final report writing
- **📅 Aug 15-20**: Presentation preparation

## Technical Stack

| Tool/Framework | Purpose | Status |
|----------------|---------|---------|
| **GitHub API** | Repository metadata and file access | ✅ Implemented |
| **Python/Jupyter** | Data processing (`pandas`, `seaborn`, `matplotlib`) | ✅ Ready |
| **Quarto** | Reproducible reports and publication output | ✅ Ready |
| **LaTeX** | Typesetting for final report | ✅ Ready |
| **R** | Statistical modeling (optional) | 📋 Available |

## Expected Results

Based on pilot analysis and literature review:

- **Stronger prompt-level correlations**: More meaningful associations may emerge with detailed prompt features
- **Complexity as engagement signal**: Advanced prompt types (few-shot, chain-of-thought) expected in high-engagement repositories
- **Collaborative authorship patterns**: Multi-contributor prompts may correlate with higher project activity
- **Temporal sophistication trends**: 2023-2024 repositories expected to show more advanced prompt structures

## Research Limitations

- **GitHub API rate limits** restrict data collection volume
- **Heuristic-based prompt extraction** may introduce noise or miss edge cases
- **Engagement metrics are proxies** for actual developer activity/quality
- **Scope limited** to Python repositories and GitHub ecosystem
- **Weak early correlations** suggest complex, potentially non-linear relationships

## Data Sources & References

### Primary Datasets
- [matched_repositories.csv](data/matched_repositories.csv): Keyword-matched repositories
- [repo_metadata.csv](data/repo_metadata.csv): GitHub metadata
- [combined_repository_data.csv](data/combined_repository_data.csv): Merged analysis dataset

### Key Literature
- Tafreshipour et al. (2024): *Prompting in the Wild: An Empirical Study of Prompt Evolution*
- Zhou et al. (2024): *A Systematic Survey of Prompt Engineering in Large Language Models*
- Li et al. (2023): *ROSCOE: A Benchmark for Reasoning Over Chain-of-Thought Explanations*

## AI Assistance Disclosure

Portions of this project (topic brainstorming, paper identification, text drafting, coding assistance) were generated with assistance from OpenAI's ChatGPT-4o. All content has been critically reviewed, edited, and verified by the author. AI tools were used to enhance productivity and clarity, not to replace original analysis or decision-making.

---

*This project contributes to understanding how prompt engineering practices relate to software project success and collaboration patterns in the era of LLM-integrated development.*