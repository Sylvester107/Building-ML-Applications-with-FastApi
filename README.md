# Building API For machine learning Model ✨

# Table of Contents
- [Sepsis Prediction API](#sepsis-prediction-api)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
  - [API Endpoints](#api-endpoints)
  - [Usage](#usage)
    - [Example curl command](#example-curl-command-to-perform-sepsis-classification)
  - [Dependencies](#dependencies)
  - [Acknowledgments](#acknowledgments)


 ## Description 📖
=================

In this project, We developed a machine learning model to identify if a patient has sepsis disease and created an API using FastAPI for the model. The API was containerized in Docker and deployed on huggingface.co.

## Getting Started ⭐

To get started with the Sepsis Prediction API, follow the steps below:

## Prerequisites 🧾

- Docker: Make sure you have Docker installed on your machine.
- You can still run it without installing Docker

## Installation 🛹

1. Clone this repository to your local machine:

   ```bash
   git clone https:https://huggingface.co/junr_syl

2. Navigate to the repository directory:
    cd api-sepsis-classifier

3. Build the Docker image:
    docker build -t {ImageName} .

4. Run the Docker container:
    docker run -d -p 7860:7860 {container_name}

The API will now be accessible at http://127.0.0.1:8000/docs#/default/sepsis_classification_classify_post.

## API Endpoints 🔎

| Endpoint                            | URL                                                        | Method | Description                                               |
| ----------------------------------- | ---------------------------------------------------------- | ------ | --------------------------------------------------------- |
| Root Endpoint                      | https://junr-syl-api-sepsis-classifier.hf.space/root__get                                    | GET    | Provides basic information about the Sepsis Prediction API. |
| Sepsis Classification Endpoint     | https://junr-syl-api-sepsis-classifier.hf.space/docs#/default/sepsis_classification_classify_post | POST   | Accepts patient data and performs sepsis classification. Provides the prediction and confidence scores. |
| [Sepsis Prediction Article](https://medium.com/jaroyajo/sepsis-prediction-app-for-icu-patients-19304598dfd3) | - | - | Learn more about this app and its development in our Sepsis Prediction article. |


## Usage ⌚
You can interact with the API using tools like curl, web browsers, or API testing tools like Postman.

### Example curl command to perform sepsis classification: 🏳
    curl -X POST -H "Content-Type: application/json" -d '{
  "PlasmaGlucose": 120,
  "BloodWorkResult_1": 4,
  "BloodPressure": 80,
  "BloodWorkResult_2": 7,
  "BloodWorkResult_3": 9,
  "BodyMassIndex": 25.5,
  "BloodWorkResult_4": 12.5,
  "Age": 50
}'https://junr-syl-api-sepsis-classifier.hf.space/docs#/default/sepsis_classification_classify_post

Huggingface Home: https://huggingface.co/spaces/junr_syl/api-sepsis-classifier

## Dependencies
    - pytest
    - scikit-learn
    - fastapi[all]
    - pydantic
    - uvicorn
    - pypi-json
    - requests
    - pandas
    - tabulate

This project is licensed under the MIT License.

## Acknowledgments 👏
This project was developed as part of the Azubi Africa Data Analysis LP6 Project. We would like to thank all contributors for their valuable insights and efforts.

For more information, feel free to contact me at sylvester.ampomah@azubiafrica.org or sylvesterjnr87@gmail.com.

## Github link:
    https://github.com/Sylvester107/Building-ML-Applications-with-FastApi.git
