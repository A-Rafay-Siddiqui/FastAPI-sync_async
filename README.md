# FAST API Sync_Async (Sych-Test)
# Abdul Rafay Siddiqui - siddiqui.arafay01@gmail.com

## Overview

This project implements a simple web application server for ZypherAI, an innovative platform for machine learning model deployment and inference. The server allows users to run predictions with machine learning models, simulating the prediction process using a mock function.

## Approach

The project is implemented using the FastAPI Python framework for building web APIs. It includes two main parts:

1. **Synchronous Model Prediction**: Implements a `/predict` endpoint that accepts POST requests with input data and returns predictions synchronously.

2. **Asynchronous Model Prediction**: Enhances the `/predict` endpoint to support asynchronous request processing. Requests can be made with an `Async-Mode: true` header to trigger asynchronous processing. The server responds with a 202 status code and a unique prediction ID, and then processes the request asynchronously.

## Instructions to Run

To run the web application server, follow these steps:

1. Clone the repository to your local machine:

    git clone https://github.com/your_username/zypherai-web-app.git
    

2. Navigate to the project directory:

    cd sychtestrafay-app

3. Install the required dependencies:

    pip install -r requirements.txt

4. Build the Docker image:

    docker build -t zypherai-app .

5. Run the Docker container:

    docker run -d -p 8000:8000 sychtestrafay-app

6. Access the application in your web browser at `http://localhost:8000`.

## Assumptions

- It is assumed that the mock model prediction function adequately simulates the behavior of a real machine learning model.
- No persistent storage is implemented for prediction results. Results are stored in memory only for the duration of the server runtime.

## Alternative Approaches

One alternative approach could be to use a different web framework, such as Flask, instead of FastAPI. However, FastAPI was chosen for its simplicity, performance, and built-in support for asynchronous request handling.

Another alternative approach could be to implement persistent storage for prediction results using a database or a message queue system. This could allow for scalability and fault tolerance, especially in production environments with high traffic.
