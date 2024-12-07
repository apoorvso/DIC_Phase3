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

Follow the steps below to set up and run the application locally with Django and ensure scikit-learn version 1.5.1 is installed.Make sure you have python 3.12

1. **Clone the Repository**:
   - Clone the project repository from GitHub:
     ```bash
     git clone https://github.com/apoorvso/crop_yield_predictor.git
     ```
   - Navigate into the project directory:
     ```bash
     cd your-repo
     ```

2. **Create a Virtual Environment (Recommended)**:
   It's best to use a virtual environment to manage dependencies. Run the following commands:
   - For Windows:
     ```bash
     python -m venv venv
     .\venv\Scripts\activate
     ```
   - For macOS/Linux:
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```

3. **Install Required Dependencies**:
   - Install the required Python dependencies listed in `requirements.txt`:
     ```bash
     pip install -r requirements.txt
     ```

4. **Ensure scikit-learn version 1.5.1**:
   - Check the currently installed version of scikit-learn:
     ```bash
     pip show scikit-learn
     ```
   - If the installed version is not 1.5.1, you can install the correct version using:
     ```bash
     pip install scikit-learn==1.5.1
     ```

5. **Run Database Migrations**:
   - Apply the database migrations to set up the database schema:
     ```bash
     python manage.py migrate
     ```

6. **Start the Django Development Server**:
   - Run the Django development server:
     ```bash
     python manage.py runserver
     ```
   - The application will be available at `http://127.0.0.1:8000/` in your browser.

7. **Access the Application**:
   - Open your browser and go to `http://127.0.0.1:8000/` to access the application locally.

---
