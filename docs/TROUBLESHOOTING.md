# Troubleshooting Guide

This guide provides solutions to common issues that you may encounter while setting up or using the Face Recognition API - FaceNet | FastAPI.

## Table of Contents

1. [Installation Issues](#1-installation-issues)
2. [API Usage Problems](#2-api-usage-problems)
3. [Common Errors](#3-common-errors)

---

## 1. Installation Issues

### Issue: Python Version Compatibility

**Problem:** You encounter issues with Python version compatibility during installation.

**Solution:** Ensure that you are using Python 3.x, as the project is designed to work with Python 3. You can check your Python version by running `python --version`.

### Issue: Missing Virtual Environment

**Problem:** You forgot to create and activate a virtual environment before installing dependencies.

**Solution:** Create a virtual environment using `virtualenv` or `conda` and activate it as described in the [Installation Guide](INSTALLATION.md).

### Issue: Dependency Installation Fails

**Problem:** You are facing problems while installing dependencies from `requirements.txt`.

**Solution:** Try the following:

- Ensure that you are in your virtual environment.
- Make sure you have an active internet connection.
- Double-check that you are using the correct version of `pip` and `python`.

### Issue: Unable to Start the Server

**Problem:** You cannot start the FastAPI development server.

**Solution:** Check for the following:

- Verify that the virtual environment is activated.
- Ensure that you are running the `uvicorn` command in the correct directory (the project root directory).

---

## 2. API Usage Problems

### Issue: API Endpoint Not Responding

**Problem:** You cannot access the API endpoints, or they are not responding as expected.

**Solution:** Troubleshoot the issue by doing the following:

- Verify that the FastAPI development server is running.
- Check if the API endpoints are accessible at the specified URLs (e.g., [http://localhost:8000/docs](http://localhost:8000/docs) for Swagger UI).

### Issue: Incorrect API Requests

**Problem:** Your API requests are not working as intended.

**Solution:** Ensure that you are using the correct HTTP methods (e.g., POST for image uploads) and providing valid request parameters according to the API documentation.

---

## 3. Common Errors

### Issue: File Upload Errors

**Problem:** You encounter issues with file uploads when using the API.

**Solution:** Check the following:

- Ensure that you are using the correct field name for file uploads in your requests (e.g., `"image"`).
- Confirm that the file you are uploading is in a supported format (e.g., JPEG or PNG).

### Issue: Rate Limiting

**Problem:** Your requests are being rate-limited by the API.

**Solution:** Be aware of any rate limiting imposed by the API and adhere to the limits. Consider optimizing your requests or contacting the API owner for increased limits if needed.

---

If you continue to experience issues that are not covered in this troubleshooting guide, please feel free to open an issue in the [GitHub repository](https://github.com/carolinajimenez/Face-Recognition-API-FaceNet-FastAPI) for further assistance.
