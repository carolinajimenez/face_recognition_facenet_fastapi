# API Usage Guide

This guide provides an overview of how to use the Face Recognition API - FaceNet | FastAPI for facial recognition tasks. It covers the available endpoints, request parameters, and example usage.

## Available Endpoints

The API provides the following endpoints:

1. **Detect Faces in an Image**

   - **Endpoint:** `/detect`
   - **Method:** POST
   - **Description:** Detects faces in an uploaded image.
   - **Request Parameters:**
     - `image` (file): The image file containing faces for detection.
   - **Response:**
     - `success` (boolean): Indicates whether the operation was successful.
     - `message` (string): A message describing the result.
     - `faces` (list): A list of detected faces, each containing information about the bounding box and facial landmarks.

2. **Recognize Faces**

   - **Endpoint:** `/recognize`
   - **Method:** POST
   - **Description:** Recognizes faces in an uploaded image.
   - **Request Parameters:**
     - `image` (file): The image file containing faces for recognition.
   - **Response:**
     - `success` (boolean): Indicates whether the operation was successful.
     - `message` (string): A message describing the result.
     - `recognized_faces` (list): A list of recognized faces, each containing information about the recognized person and confidence score.

## Example Usage

### Detect Faces in an Image

**Request:**

```bash
curl -X POST "http://localhost:8000/detect" -H "accept: application/json" -H "Content-Type: multipart/form-data" -F "image=@path/to/your/image.jpg"
```

**Response (Sample):**

```json
{
  "success": true,
  "message": "Faces detected successfully.",
  "faces": [
    {
      "bounding_box": {
        "top": 100,
        "left": 200,
        "width": 50,
        "height": 50
      },
      "landmarks": {
        "left_eye": [220, 120],
        "right_eye": [260, 120],
        // Other facial landmarks
      }
    },
    // Additional detected faces
  ]
}
```

### Recognize Faces

**Request:**

```bash
curl -X POST "http://localhost:8000/recognize" -H "accept: application/json" -H "Content-Type: multipart/form-data" -F "image=@path/to/your/image.jpg"
```

**Response (Sample):**

```json
{
  "success": true,
  "message": "Faces recognized successfully.",
  "recognized_faces": [
    {
      "person_name": "John Doe",
      "confidence": 0.92
    },
    // Additional recognized faces
  ]
}
```

### Error Handling

If there is an issue with the API request, you will receive an error response with a descriptive message.
Refer to the [Troubleshooting Guide](docs/TROUBLESHOOTING.md) for common issues and solutions.

### Rate Limiting

To prevent abuse, the API may have rate limiting in place. Ensure you are aware of and adhere to any rate limits imposed by the API.
