# FastAPI on Vercel

A FastAPI application deployed on Vercel, featuring profile retrieval and email sending functionality.

## Project Description

This repository contains a FastAPI application that provides API endpoints for retrieving user profiles and simulating email sending. The application is designed to be deployed on Vercel and includes a simple HTML frontend.

## Scripts

### main.py

The main script that defines the FastAPI application and its endpoints.

#### Features:

- Serves a static HTML page at the root URL
- Provides a `/getProfile` endpoint to retrieve user profiles
- Offers a `/sendEmail` endpoint to simulate email sending
- Uses FastAPI's dependency injection for input validation
- Serves static files (favicon)

#### Usage:

1. Deploy the application to Vercel or run it locally
2. Access the root URL to see the HTML frontend
3. Use the `/docs` or `/redoc` endpoints to interact with the API
4. Send GET requests to `/getProfile` with an email parameter
5. Send POST requests to `/sendEmail` with an email in the request body

## Common Features

- FastAPI framework for building APIs
- Vercel deployment support
- HTML frontend served at the root URL
- API documentation with Swagger UI and ReDoc

## Requirements

- Python 3.9+
- FastAPI
- Uvicorn (for local development)

## Installation

To set up the project locally, follow these steps:

```bash
# Create and activate the Conda environment
conda create --name FastAPIVercel python=3.9
conda activate FastAPIVercel

# Install the required packages
pip install fastapi uvicorn
```

## Running the Application

To run the application locally:

```bash
uvicorn main:app --reload
```

The application will be available at `http://localhost:8000`.

## Note

This application is designed to be deployed on Vercel. Make sure to configure your Vercel project settings appropriately, including the Python version and build commands.

The `/getProfile` endpoint currently only returns a profile for the email "johndoe@example.com". For all other emails, it returns a generic message.

The `/sendEmail` endpoint simulates sending an email but does not actually send one. In a production environment, you would need to implement actual email sending functionality.
