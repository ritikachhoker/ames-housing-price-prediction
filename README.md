# Ames Housing Price Prediction 🏡

A Machine Learning project that predicts house sale prices using **SGDRegressor** with a preprocessing pipeline. The project includes a **FastAPI backend**, a **Streamlit frontend**, and **Docker Compose** for running both services together.

## 🚀 Features

- House price prediction using a trained Machine Learning model.
- Data preprocessing using Scikit-learn pipelines.
- Missing value imputation and feature scaling.
- Categorical feature encoding using OneHotEncoder.
- FastAPI REST API for making predictions.
- Interactive Streamlit user interface.
- Dockerized API and frontend.
- Docker Compose to run both services together.

## 🛠️ Tech Stack

- **Language:** Python
- **Machine Learning:** Scikit-learn, Pandas, NumPy
- **Backend:** FastAPI, Uvicorn
- **Frontend:** Streamlit
- **Model:** SGDRegressor
- **Containerization:** Docker, Docker Compose
- **API Testing:** FastAPI Swagger UI

## 📂 Project Structure

```text
home_price_prediction_sgdregressor/
│
├── app.py
├── main.py
├── Dockerfile
├── docker-compose.yml
├── requirement.txt
│
├── model/
│   └── model.pkl
│
└── README.md
```

*Note: Adjust the filenames above if your actual project structure is different.*

## ⚙️ Run Locally with Docker Compose

### Prerequisites

- Docker Desktop installed and running.
- Git (optional, for cloning the repository).

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd home_price_prediction_sgdregressor
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### 2. Build and start the services

```bash
docker compose up --build
```

Docker Compose builds the required images and starts the API and frontend containers.

### 3. Open the application

| Service | URL |
|---|---|
| Streamlit Frontend | http://localhost:8501 |
| FastAPI Swagger Docs | http://localhost:8000/docs |

Enter the required house features in the Streamlit interface to get a predicted sale price.

### 4. Stop the application

Press `Ctrl + C` in the terminal, then run:

```bash
docker compose down
```

## 🐳 Docker Hub Images

The project images are available on Docker Hub:

- **API:** [ritichh/ames-housing-api](https://hub.docker.com/r/ritichh/ames-housing-api)
- **Frontend:** [ritichh/ames-housing-frontend](https://hub.docker.com/r/ritichh/ames-housing-frontend)

To download the images:

```bash
docker pull ritichh/ames-housing-api:latest
docker pull ritichh/ames-housing-frontend:latest
```

To run the complete application, use the project's Docker Compose configuration.

## 🔌 API Usage

Open the Swagger documentation:

http://localhost:8000/docs

Use the available prediction endpoint to submit the required input features and inspect the API response.

The exact endpoint path and input schema are defined in `main.py`.

## 🧠 Machine Learning Workflow

1. Exploratory Data Analysis (EDA).
2. Data cleaning and missing value handling.
3. Feature selection and feature engineering.
4. Train-test split.
5. Preprocessing pipeline construction.
6. Model training using SGDRegressor.
7. Model evaluation using R² score and other regression metrics.
8. Saving the trained pipeline for inference.
9. Integrating the model with FastAPI and Streamlit.
10. Containerizing the application using Docker.

## 📊 Model Evaluation

The model was evaluated using regression metrics, including the R² score.

- **Training R²:** 0.8090880378719172
- **Testing R²:**  0.8370141769582473
- **MAE:** 20563.17683849547

Use the actual values from your final model evaluation rather than estimated results.

## 🔮 Future Improvements

- Deploy the application to a cloud platform.
- Add automated tests for the API and preprocessing pipeline.
- Improve model performance through further experimentation.
- Set up a CI/CD workflow.
- Add application screenshots and a live demo link.

## 👩‍💻 Author

**Ritika Chhoker**

MCA Student | Aspiring AI/ML Engineer

GitHub: [ritikachhoker](https://github.com/ritikachhoker)

---

If you found this project interesting, feel free to explore the repository and share feedback!
