Face Recognition API - FaceNet | FastAPI
==============================

This project is a facial recognition API using FaceNet technology and built with FastAPI. It enables the detection and recognition of faces in images, making it suitable for a wide range of applications in security, automation, and data analysis.

## Key Features

- **Accurate facial recognition:** It utilizes the FaceNet model to achieve high accuracy in identifying faces.

- **Interactive API:** Based on FastAPI, this API is easy to use and provides an interactive interface for testing and utilizing its capabilities.

- **Comprehensive documentation:** The documentation included in this repository provides detailed instructions on how to install and use the API.

## How to Use

1. **Installation:**

   Follow the installation instructions detailed in the [documentation](docs/INSTALLATION.md) to set up the development environment.

2. **Execution:**

   Start the development server using the command:

    ```
    uvicorn src.main:app --host 0.0.0.0 --port 8000 --reload
    ```

    You can now access the API via your browser or tools like [Swagger UI](http://localhost:8000/docs) or [ReDoc](http://localhost:8000/redoc) to interact with it.

3. **Integration into Your Application:**

    Refer to the [API usage documentation](docs/API_USAGE.md) for information on integrating this API into your project.

## License

This project is distributed under the [MIT License](LICENSE), which means you can use, modify, and distribute the software in accordance with the terms of the license.


## Project Organization

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    └── src                <- Source code for use in this project.
        ├── __init__.py    <- Makes src a Python module
        │
        ├── data           <- Scripts to download or generate data
        │   └── make_dataset.py
        │
        ├── features       <- Scripts to turn raw data into features for modeling
        │   └── build_features.py
        │
        ├── models         <- Scripts to train models and then use trained models to make
        │   │                 predictions
        │   ├── predict_model.py
        │   └── train_model.py
        │
        └── visualization  <- Scripts to create exploratory and results oriented visualizations
            └── visualize.py
--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
