# Installation Guide

This guide provides step-by-step instructions for setting up and installing the Face Recognition API - FaceNet | FastAPI on your local development environment.

## Prerequisites

Before you begin, ensure you have the following prerequisites installed:

- Python 3.x
- Virtual environment tool (e.g., `virtualenv` or `conda`)
- Git (optional, but recommended)

## Installation Steps

Follow these steps to install and run the Face Recognition API:

1. **Clone the Repository**

   If you have Git installed, you can clone the repository using the following command:

   ```bash
   git clone https://github.com/carolinajimenez/Face-Recognition-API-FaceNet-FastAPI.git
   ```

    Alternatively, you can download the repository as a ZIP file and extract it.

2. **Navigate to the Project Directory**

    Change your working directory to the project folder:

    ```
    cd face_recognition_facenet_fastapi
    ```

3. **Create and Activate a Virtual Environment**

    It's recommended to use a virtual environment to isolate dependencies. Create one using `virtualenv` or `conda`.

4. **Install Dependencies**

    Install the required Python packages from the requirements.txt file:

    ```
    pip install -r requirements.txt
    ```

6. **Run the FastAPI Application**

    Start the FastAPI development server:

    ```
    uvicorn src.main:app --host 0.0.0.0 --port 8000 --reload
    ```

    This will launch the API, and you can access it in your web browser or via tools like [Swagger UI](http://localhost:8000/docs) or [ReDoc](http://localhost:8000/redoc).

