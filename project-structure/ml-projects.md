# Common Folder Structures for Machine Learning Projects

A well-structured project folder is essential for maintainability, collaboration, reproducibility, and scalability in machine learning (ML) projects. While there is no single "correct" structure, several best practices and templates have emerged in the ML community.

### Typical ML Project Folder Structure

A widely adopted structure, inspired by the Cookiecutter Data Science template and common in both academic and industry settings, looks like this:

```
project_name/
├── README.md
├── data/
│   ├── raw/         # Original, immutable data dumps
│   ├── processed/   # Cleaned/feature-engineered datasets
│   ├── interim/     # Intermediate data (optional)
│   └── external/    # Third-party data
├── notebooks/
│   ├── 01-eda.ipynb
│   ├── 02-modeling.ipynb
│   └── archive/
├── src/
│   ├── __init__.py
│   ├── data/        # Data loading, preprocessing scripts
│   ├── features/    # Feature engineering scripts
│   ├── models/      # Model definitions and training scripts
│   ├── visualization/ # Plotting and analysis scripts
│   └── utils/       # Helper functions
├── models/          # Serialized models, checkpoints
├── scripts/         # Standalone scripts for running tasks
├── results/         # Generated results, metrics, plots
├── docs/            # Documentation, design docs
├── requirements.txt or environment.yml
├── .gitignore
└── tests/           # Unit and integration tests
```

This structure can be further expanded or customized based on project needs[^1][^2][^3][^4][^5][^6].

### Key Principles

- **Separation of concerns:** Raw data, code, notebooks, and results are clearly separated.
- **Reproducibility:** Scripts, requirements, and configuration files ensure others can rerun experiments.
- **Scalability:** Easy to add new models, data sources, or features.
- **Collaboration:** New team members can quickly understand and contribute.


### Example: Cookiecutter Data Science

The [Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/) template is a popular starting point. Its structure is widely used and recommended in ML and data science[^1][^3][^4].

### Detailed Example from GitHub

From the [YKatser/ml-project-template][^3]:

```
├── README.md
├── data/
│   ├── raw/
│   ├── interim/
│   ├── processed/
│   └── external/
├── models/
├── notebooks/
├── docs/
├── results/
├── .gitignore
├── requirements.txt
└── src/
```

This template includes clear separation for data at different processing stages, notebooks, code, models, and documentation[^3].

### More Advanced Example

For deep learning or larger ML projects, you might see even more granular divisions, such as:

- `src/data_pipeline/` for data ingestion and augmentation
- `src/models/architectures/` for different network architectures
- `src/training/experiments/` for experiment tracking and configuration
- `src/inference/` for deployment scripts
- `src/testing/` for unit and integration tests[^5]


### Real Practice Examples from GitHub

- [Viveckh/LilHomie](https://github.com/Viveckh/LilHomie): Predicts housing prices, includes folders for web scraping, EDA, modeling, and results[^7].
- [mandliya/ml](https://github.com/mandliya/ml): Daily ML/DL projects, organized by concept and project[^7].
- [Priyansh42/Lung-Cancer-Detection](https://github.com/Priyansh42/Lung-Cancer-Detection): Follows a structure with separate folders for data, models, and notebooks[^8].
- [dushyant18033/BTC-Price-Prediction-ML-Project](https://github.com/dushyant18033/BTC-Price-Prediction-ML-Project): Organized into data, scripts, and results[^8].
- [ashishpatel26/500-AI-Machine-learning-Deep-learning-Computer-vision-NLP-Projects-with-code](https://github.com/ashishpatel26/500-AI-Machine-learning-Deep-learning-Computer-vision-NLP-Projects-with-code): A massive collection of real-world ML projects, each with its own structure[^9].

You can browse these repositories for practical, real-world folder structures and adapt them to your needs.

## Summary Table: Typical Folders and Their Purpose

| Folder | Purpose |
| :-- | :-- |
| `data/` | Stores raw, processed, interim, and external datasets |
| `notebooks/` | Jupyter notebooks for EDA, modeling, and analysis |
| `src/` | Source code: data loaders, feature engineering, models, utils |
| `models/` | Saved models, checkpoints, and predictions |
| `scripts/` | Standalone scripts for specific tasks |
| `results/` | Generated results, plots, and reports |
| `docs/` | Project documentation and design docs |
| `requirements.txt`/`environment.yml` | Environment and dependency management |
| `tests/` | Unit and integration tests |

## Further Resources

- [Cookiecutter Data Science Template][^1][^3][^4]
- [Full Stack Deep Learning Course](https://fullstackdeeplearning.com/course/2022/) (for more on tools and workflow)[^10]
- [500+ ML Projects with Code][^9]

A clear folder structure will help your ML project remain organized, reproducible, and collaborative, whether you're working solo or in a team.

<div style="text-align: center">⁂</div>

[^1]: https://towardsdatascience.com/structuring-your-machine-learning-project-with-mlops-in-mind-41a8d65987c9/

[^2]: https://gist.github.com/ericmjl/27e50331f24db3e8f957d1fe7bbbe510

[^3]: https://github.com/YKatser/ml-project-template

[^4]: https://dev.to/luxdevhq/generic-folder-structure-for-your-machine-learning-projects-4coe

[^5]: https://gist.github.com/Nivratti/ea81e952e07ffbbf03e6d44a7dbbef8f

[^6]: https://www.linkedin.com/pulse/ideal-way-setup-machine-learning-projects-tito-osadebey-4i1zf

[^7]: https://github.com/topics/machine-learning-projects

[^8]: https://github.com/topics/machine-learning-project

[^9]: https://github.com/ashishpatel26/500-AI-Machine-learning-Deep-learning-Computer-vision-NLP-Projects-with-code

[^10]: https://www.reddit.com/r/learnmachinelearning/comments/16j9wot/how_to_best_structure_a_ml_project/

