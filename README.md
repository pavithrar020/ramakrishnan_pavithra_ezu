# README: Course Info Django Project

## Overview
This Django project is a course information management system designed to handle data related to courses, instructors, students, and registrations. It includes models, templates, and static files for managing and displaying course-related data.

---

## Project Structure

### Root Directory
- **`.idea/`**: Contains IDE-specific settings and configurations.
- **`requirements/`**: Dependencies for the project.
  - **`base.txt`**: Lists the required Python packages.
- **`db.sqlite3`**: SQLite database file.
- **`manage.py`**: Django’s command-line utility for running the development server and managing the project.

### Application Directory: `courseinfo/`
Contains the core logic and files for the application.

#### **Directories**
- **`archived_migrations/`**: Older migration files for database changes.
- **`migrations/`**: Active migration files.
- **`static/`**: Contains static assets like CSS, JS, and images.
  - **`css/`**: Styling for the application.
  - **`img/`**: Icons and images used in the project.
  - **`js/`**: JavaScript for dynamic functionality.
- **`templates/courseinfo/`**: HTML templates for the application.

#### **Key Files**
- **`models.py`**: Defines the database schema for courses, instructors, students, and registrations.
- **`views.py`**: Contains class-based views (GCBV) for handling requests and rendering templates.
- **`urls.py`**: Maps URLs to views.
- **`forms.py`**: Handles forms for creating and updating objects.
- **`utils.py`**: Utility functions for reusable logic.
- **`admin.py`**: Configuration for the Django admin interface.

### Static and Template Files
- **CSS**:
  - `base.css`: Base styles for the application.
  - `normalize.css` & `skeleton.css`: External libraries for consistent styling.
  - Custom styles for forms, login, and navigation.
- **Templates**:
  - Templates for listing, viewing, creating, updating, and deleting courses, instructors, students, and registrations.
  - Includes a base template for consistent layout.

### Settings
- **`settings/`**: Contains environment-specific settings.
  - **`base.py`**: Shared settings for all environments.
  - **`development.py`**: Development-specific settings.
  - **`production.py`**: Production-specific settings.

---

## Key Features
1. **User Authentication**:
   - Login functionality with a dedicated template.
2. **CRUD Operations**:
   - Create, read, update, and delete (CRUD) functionality for courses, instructors, students, and registrations.
   - Templates to confirm or refuse deletions.
3. **Pagination**:
   - Pagination plans included for optimizing list views.
4. **Responsive Design**:
   - Mobile-friendly and responsive layouts using Skeleton CSS.
5. **Static Assets**:
   - Custom icons and visual elements for better UI/UX.

---

## Prerequisites
- **Python**: 3.8 or higher
- **Django**: 3.2 or higher
- **Dependencies**:
  Install all required packages from `requirements/base.txt`:
  ```bash
  pip install -r requirements/base.txt
  ```

---

## How to Run
1. **Set Up Environment**:
   - Create and activate a virtual environment:
     ```bash
     python -m venv venv
     source venv/bin/activate  # On Windows: venv\Scripts\activate
     ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements/base.txt
   ```
3. **Apply Migrations**:
   ```bash
   python manage.py migrate
   ```
4. **Run the Server**:
   ```bash
   python manage.py runserver
   ```
5. **Access the Application**:
   Open your browser and navigate to `http://127.0.0.1:8000/`.

---

## Customization
- **Static Content**:
  - Modify styles in `static/css/` and scripts in `static/js/` to customize the look and feel.
- **Templates**:
  - Update or extend templates in `templates/courseinfo/` for custom pages or layouts.
- **Models**:
  - Extend `models.py` to include additional fields or entities.
- **Environment Settings**:
  - Use `development.py` for local development and `production.py` for deployment.

---

## Future Enhancements
- Add user roles and permissions for instructors and students.
- Integrate advanced filtering and search functionality for courses.
- Improve reporting and analytics capabilities with dynamic charts and graphs.
- Deploy to a production environment using tools like Gunicorn and Nginx.
