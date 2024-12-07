# Project Submission - Phase 3

**Prison Data Analysis Project**  
**Authors**: FNU Syed Zubair Ahmed, Apoorv Sood, Jainam Manish Jain, Kalash Thakur  
**Project Name**: Predicting Crime Rates and Enhancing Resource Allocation Strategies Using Prison Data  
**Professor Name**: Prof. Chen Xu  

---

## Team Members and Questions 

| Team Member           | Question                                                                                                     | Code Location                       | Report Location                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------|-------------------------------------|
| Jainam Manish Jain     | Rates of Escape and Mental Illness vs. Educational Infrastructure: Identify relationships between inmate education programs and outcomes. | `predictions/views.py` - line 149 function-predict_view_2 | `predictions/views.py` (lines 50–100) |
| Kalash Thakur          | Proportion of Undertrial vs. Convicted Inmates Across States and Crimes: Analyze judicial inefficiencies.    | `predictions/views.py` - line 197 function-predict_view_3 | `predictions/models/random_forest_model.pkl` |
| FNU Syed Zubair Ahmed | Predicting Prison Budget Allocations: Explore historical overcapacity and expenditure data for insights.    | `predictions/views.py` - line 245 function-predict_view_4 | `hypothesis/settings.py` (lines 250–300) |
| Apoorv Sood            | Demographic Analysis of Inmate Populations: Classify inmates as undertrial or convicted by demographics.     | `predictions/views.py` - line 102 function-predict_view_1 | `predictions/templates/predict.html` |

---

## Project Structure

- **README.md**: Contains project details, team member contributions, and folder structure.
- **db.sqlite3**: SQLite database containing project data.
- **directory_structure.txt**: Text file with the full directory tree.
- **manage.py**: Django management script for running the project.
- **requirements.txt**: Python dependencies for the project.

### Main Application Structure

- **crop_yield_predictor/**: Core project settings and configuration files.
  - `asgi.py`: ASGI application entry point.
  - `settings.py`: Project settings.
  - `urls.py`: URL routing for the application.
  - `wsgi.py`: WSGI configuration for deployment.
  - `__init__.py`: Marks the directory as a Python package.
  - **__pycache/**: Compiled Python files.
    - Various `.pyc` files for `settings.py`, `urls.py`, and `wsgi.py`.

- **predictions/**: Application logic, including models, views, and templates.
  - **migrations/**: Database migration files.
    - Includes various migration scripts like `0001_initial.py` and others.
  - **models/**: Pre-trained machine learning models.
    - Includes models for budget prediction, crime prediction, and classification.
  - **static/**: Static assets, including CSS, JavaScript, and images.
    - `images/`: Contains visual assets like plots and graphs.
    - `predictions/`: CSS and JS for prediction views.
  - **templates/**: HTML templates for rendering views.
    - `predict.html`: Main prediction page.
    - `Home.html`: Home page for the application.
    - Other templates for login, profile, and various prediction forms.
  - **__pycache/**: Compiled Python files for models, views, and other logic.

- **static/**: Global static files for admin and project assets.
  - `admin/`: Admin-specific styles and scripts.
    - Includes CSS and JavaScript files for the admin interface.
  - `images/`: Contains various project images.
  - `predictions/`: Static files for the predictions app.
    - Includes CSS, JS, and images used in the predictions page.

---

## Instructions to Build the App

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo.git
   cd your-repo
