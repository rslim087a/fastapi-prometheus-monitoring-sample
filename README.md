# FastAPI Metrics App

This is a FastAPI application with Prometheus metrics integration.

## Prerequisites

- Python 3.9 or higher
- pip (Python package installer)
- Postman (optional, for testing API endpoints)

## Setup and Running the Application

1. Ensure you have the source code (`app.py`) and `requirements.txt` file in your project directory.

2. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   ```

3. Activate the virtual environment:
   - On Windows:
     ```
     venv\Scripts\activate
     ```
   - On macOS and Linux:
     ```
     source venv/bin/activate
     ```

4. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

5. Run the application:
   ```
   uvicorn app:app --host 0.0.0.0 --port 8000
   ```

   The application will start and be available at http://localhost:8000

## API Endpoints

- GET /: Root endpoint
- POST /items: Create a new item
- GET /items/{item_id}: Retrieve an item
- PUT /items/{item_id}: Update an item
- DELETE /items/{item_id}: Delete an item
- GET /metrics: View Prometheus metrics

## Testing with Postman

A Postman collection (`fastapi-metrics-postman-collection.json`) is provided for testing the API endpoints. To use it:

1. Open Postman
2. Click on "Import" and select the JSON file
3. The collection "FastAPI Metrics App" will be added to your Postman workspace
4. You can now use the pre-configured requests to test each endpoint

## Stopping the Application

To stop the application, press CTRL+C in the terminal where it's running.

Remember to deactivate the virtual environment when you're done:
```
deactivate
```