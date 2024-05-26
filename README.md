# Recipe Management Application

This project consists of a Python Flask application and associated testing files that manage a simple recipe database. The application allows for creating, updating, deleting, and querying recipes.

## File Descriptions

### Python Files
- **app.py**: The main Flask application file. It contains routes for handling API requests such as listing all recipes, retrieving detailed information about a specific recipe, creating new recipes, updating existing ones, and deleting recipes. It also includes error handling and data validation using Pydantic.
- **schemas.py**: Defines Pydantic schemas for data validation. This file ensures that the recipes meet the specified requirements, such as title length and ingredient checks against profanity.
- **test_recipes.py**: Contains unit tests for the Flask application using pytest. Tests ensure that each endpoint correctly handles various operations under different conditions.
- **test_recipes_v2.py**: An alternative set of tests that might be used for different configurations or testing environments.

### Functionality
- The **app.py** file sets up a Flask application with several routes, including functionality to reset the database to a default state, search recipes based on title or ingredients, and handle CRUD operations with robust data validation.
- **schemas.py** is crucial for maintaining data integrity, preventing invalid data from being entered into the system via API requests.
- Testing files (**test_recipes.py** and **test_recipes_v2.py**) are critical for verifying the functionality of the Flask routes, ensuring that they perform as expected and handle edge cases, such as invalid data inputs or requests for non-existent resources.

## Testing
- To run tests, use the command `pytest` within your virtual environment. Ensure that the Flask app is configured correctly for testing by setting the appropriate environment variables if needed.
- The tests cover a wide range of possible interactions with the API, from successful operations to attempts that should fail due to business logic or validation rules.

## Development and Deployment
- For local development, ensure you have Python and Flask installed, and run the application using `flask run` within your terminal.
- The application requires external libraries such as Flask, Pydantic, and pytest, which should be included in your `requirements.txt` file for easy setup in different environments.

This project illustrates basic best practices for API development with Flask, including the use of Pydantic for data validation and pytest for writing comprehensive tests.
