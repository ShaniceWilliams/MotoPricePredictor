# Project File Structure
.
├── data
│   ├── processed
│   │   └── cleaned_mc_data.csv        # Cleaned dataset used for training
│   └── raw
│       └── MotocycleData.csv   # Original raw dataset
├── models
│   ├── pipeline.bin          # DictVectorizer + preprocessing pipeline
│   └── model.bin                   # Trained Random Forest model
├── notebooks
│   ├── 01_eda.ipynb                # Exploratory data analysis
│   └── 02_model_building.ipynb     # Model training and evaluation
├── src
│   ├── __init__.py                 
│   ├── app.py                      # FastAPI application entry point
│   ├── logger.py                   # Logging configuration for API service
│   ├── ebay.py                     # Core prediction utilities / model loader
│   ├── models
│   │   └── pipeline.bin      # Model artifacts for API use
│   ├── pipeline
│   │   ├── __init__.py             
│   │   ├── predict.py              # API prediction logic
│   │   └── train.py                # Training script for offline model training
│   └── schemas
│       ├── __init__.py             
│       └── models.py               # Pydantic models for API validation
├── Dockerfile                      # Docker image for API deployment
├── README.md                       # Project documentation
├── pyproject.toml                  # Project dependencies and build config
└── uv.lock                         # Dependency lock file for reproducible builds