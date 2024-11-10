# JobMatchHub-Web-Scraping-Project

JobMatchHub is a comprehensive web-based job search application developed as a software engineering project. It allows users to search, filter, and save job preferences, with features for email notifications about relevant job listings. The app is built using Flask and SQLAlchemy, with mock data generation and testing utilities.

## Features

- **User Authentication**: Simple login system with pre-defined credentials.
- **Job Listings Search & Filtering**: Allows users to filter listings by job type, industry, location, salary range, remote options, and experience level.
- **Save Job Preferences**: Users can save job preferences for quick access and future searches.
- **Email Notifications**: Sends email notifications to users about job listings that match their saved search criteria.
- **Mock Job Listings Generation**: Uses Faker to generate mock job data.
- **Unit Testing**: Tests core job search functionality with various conditions and filters.
- **Sphinx Documentation**: Includes documentation setup with Sphinx.

## Project Structure

    ├── app.py                  # Main application entry point
    ├── controllers
    │   └── controllers.py       # Controller functions for handling routes and business logic
    ├── database.py              # Database initialization
    ├── fake_web_scrapper
    │   └── mock_data.py         # Mock job listings generator
    ├── models
    │   └── models.py            # Database models for User, JobSearch, and JobListing
    ├── unit_testing
    │   └── test.py              # Unit tests for job search filtering
    ├── views
    │   ├── static               # Static assets (CSS, images)
    │   └── templates            # HTML templates for application pages
    └── docs
        ├── Makefile             # Makefile for Sphinx documentation generation
        └── source               # Documentation source files

## Getting Started

### Prerequisites

Ensure Python 3.x is installed and install project dependencies with:

```bash
pip install -r requirements.txt
```

## Running the Application

### Database Setup:

Run the following to initialize the database:

```bash
flask db init
flask db migrate
flask db upgrade
```

Alternatively, app.py can use db.create_all() to initialize tables on first run.

### Start the Flask Application:
```bash
python app.py
```
Access the application at http://127.0.0.1:5000.

## Documentation
To generate HTML documentation with Sphinx:

```bash
cd docs
make html
```

## Unit Testing
Run tests with:

```bash
python -m unittest discover -s unit_testing
```

## Mock Data Generation
Mock job listings can be generated within app.py using generate_job_listings() for demonstration purposes.

## Email Notifications Setup
Requires Gmail API credentials for email notifications.

1. Generate client_secret.json: Follow Google’s guide.
2. Authenticate on First Run: The app will prompt for Gmail authentication, creating token.pickle for future use.

## Future Improvements
- Implement actual job listing scraping from external sources.
- Add more filters (e.g., company size, skills).
- Enhance user registration with password recovery.





