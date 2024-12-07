# Project Submission - Phase 3

**Prison Data Analysis Project**  
**Authors**: FNU Syed Zubair Ahmed, Apoorv Sood, Jainam Manish Jain, Kalash Thakur  
**Project Name**: Predicting Crime Rates and Enhancing Resource Allocation Strategies Using Prison Data  
**Professor Name**: Prof. Chen Xu  

---

## Team Members and Questions 

| Team Member       | Question                                                                                                     | Code Location                       | Report location                   |
|-------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------|--------------------------------------|
| Jainam Manish Jain | Rates of Escape and Mental Illness vs. Educational Infrastructure: Identify relationships between inmate education programs and outcomes. | `predictions/models/ridge_model_escapees.pkl` | `predictions/views.py` (lines 50–100) |
| Kalash Thakur       | Proportion of Undertrial vs. Convicted Inmates Across States and Crimes: Analyze judicial inefficiencies.    | `hypothesis/settings.py` (lines 150–200) | `predictions/models/random_forest_model.pkl` |
| FNU Syed Zubair Ahmed | Predicting Prison Budget Allocations: Explore historical overcapacity and expenditure data for insights.    | `predictions/models/xgboost_budget.pkl` | `hypothesis/settings.py` (lines 250–300) |
| Apoorv Sood     | Demographic Analysis of Inmate Populations: Classify inmates as undertrial or convicted by demographics.     | `predictions/views.py` - line 102 function-predict_view_1 | `predictions/templates/predict.html` |

---

## Project Structure

- **README.md**: Contains project details, team member contributions, and folder structure.
- **db.sqlite3**: SQLite database containing project data.
- **directory_structure.txt**: Text file with the full directory tree.
- **manage.py**: Django management script for running the project.
- **requirements.txt**: Python dependencies for the project.

### Main Application Structure
- **hypothesis/**: Contains core project settings and configuration files.
  - `settings.py`: Project settings.
  - `urls.py`: URL routing for the application.
  - `wsgi.py`: WSGI configuration for deployment.

- **predictions/**: Contains application logic, including models, views, and templates.
  - `models/`: Pre-trained machine learning models.
    - `ridge_model_escapees.pkl`: Ridge regression model for escape rates.
    - `random_forest_model.pkl`: Random forest model for undertrial analysis.
    - `xgboost_budget.pkl`: XGBoost model for budget prediction.
    - `logistic_regression_model.pkl`: Logistic regression for inmate classification.
  - `static/`: Static assets, including CSS, JavaScript, and images.
    - `images/`: Visualization outputs from analysis.
    - `predictions/`: CSS and JS for prediction views.
  - `templates/`: HTML templates for rendering views.
    - `predict.html`: Main prediction page.
    - `Home.html`: Home page for the application.
  - `views.py`: Main logic for handling user requests.

- **static/**: Global static files for admin and project assets.
  - `css/`: Admin and custom stylesheets.
  - `js/`: JavaScript files for interactivity.
  - `img/`: Images used in the project.

- **images/**: Additional visual assets for documentation and analysis.

---

## Instructions to Build the App

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo.git
   cd your-repo
