# WineQuality-Prediction

🚀 **Features**

End-to-End ML Pipeline
Data ingestion, validation, transformation, model training, and evaluation.
Configurable Setup
Parameters managed via params.yaml and config.yaml.
Model Deployment
app.py serves predictions (Flask/FastAPI based).
Artifacts Tracking
Stores datasets, trained models, and evaluation metrics.
CI/CD Ready
GitHub Actions workflow (.github/workflows/main.yaml).
Dockerized
Ready for containerized deployment.



📂 **Project Structure**

        wine-quality-prediction/
        │
        ├── .github/
        │   └── workflows/
        │       └── main.yaml                # CI/CD Pipeline
        │
        ├── src/
        │   └── mlproject/
        │       ├── _init_.py
        │       ├── components/
        │       │   ├── _init_.py
        │       │   ├── data_ingestion.py
        │       │   ├── data_validation.py
        │       │   ├── data_transformation.py
        │       │   ├── model_trainer.py
        │       │   └── model_evaluation.py
        │       ├── utils/
        │       │   ├── _init_.py
        │       │   ├── common.py
        │       │   └── logger.py
        │       ├── config/
        │       │   ├── _init_.py
        │       │   └── configuration.py
        │       ├── pipeline/
        │       │   ├── _init_.py
        │       │   ├── stage_01_data_ingestion.py
        │       │   ├── stage_02_data_validation.py
        │       │   ├── stage_03_data_transformation.py
        │       │   ├── stage_04_model_trainer.py
        │       │   ├── stage_05_model_evaluation.py
        │       │   └── predict.py
        │       ├── entity/
        │       │   ├── _init_.py
        │       │   └── config_entity.py
        │       └── constants/
        │           └── _init_.py
        │
        ├── config/
        │   └── config.yaml
        │
        ├── schema.yaml
        ├── params.yaml
        ├── requirements.txt
        ├── setup.py
        ├── main.py
        ├── app.py
        ├── Dockerfile
        ├── .dockerignore
        ├── research/
        │   └── experiments.ipynb
        ├── templates/
        │   ├── index.html
        │   └── results.html
        └── artifacts/
            ├── data_ingestion/
            ├── data_validation/
            ├── data_transformation/
            ├── model_trainer/
            └── model_evaluation/
        """



⚙️ **Installation & Setup**

1️⃣ **Clone the Repository**

git clone https://github.com/your-username/wine-quality-prediction.git
cd wine-quality-prediction

2️⃣ **Create Virtual Environment**

python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows

3️⃣ **Install Dependencies**

pip install -r requirements.txt

4️⃣ **Run the Pipeline**

python main.py



🧪 **Model Training & Evaluation**

Training Data: Data/winequality-red.csv

    Pipeline Steps:
    
    Data Ingestion
    Data Validation
    Data Transformation
    Model Training
    Model Evaluation

**Results are stored in the artifacts/ folder:**

Trained model → artifacts/model_trainer/model.joblib
Evaluation metrics → metrics.json



🌐 **Run the Web App**

After training, launch the API:
python app.py

🐳 **Run with Docker**

docker build -t wine-quality .
docker run -p 5000:5000 wine-quality

🔄 **CI/CD**

GitHub Actions workflow (.github/workflows/main.yaml) automates:

    Linting & Testing
    Model Training
    Deployment Steps


📊 **Dataset**

The dataset is based on red wine quality from the UCI Machine Learning Repository
Each sample includes 11 physicochemical variables (e.g., acidity, sugar, pH) and a quality score (0–10).


🛠️ **Tech Stack:**

Python 3.8+
Flask / FastAPI
Scikit-learn, Pandas, NumPy
Docker
GitHub Actions
