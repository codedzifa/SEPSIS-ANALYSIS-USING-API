# SEPSIS-ANALYSIS-USING-API

A machine learning model that seeks to learn and predict if people have SEPSIS or not.

## Introduction

In this project, we aim to create an API that might be requested to interact with an ML model. This is an interesting solution when you want to keep your model architecture secret or to make your model available to users already having an API.

## Description

We will construct a machine learning model utilizing the [Sepsis](https://www.kaggle.com/datasets/chaunguynnghunh/sepsis?select=README.md) dataset available on Kaggle. The primary objective of this model is to forecast whether a patient is afflicted with sepsis or not.

Once the model is created, we will develop an Application Programming Interface (API) using FastAPI, facilitating seamless communication with the model. The subsequent step involves deploying the API on the Hugging Face platform.

You can learn more about FastAPI here
[FastAPI](https://fastapi.tiangolo.com/).

### Dataset Description

### Data Fields

| Column Name | Labels/Features | Description                                                                |
| ----------- | --------------- | -------------------------------------------------------------------------- |
| ID          | N/A             | Unique number to represent patient ID                                      |
| PRG         | Label 1         | Plasma glucose                                                             |
| PL          | Label 2         | Blood Work Result-1 (mu U/ml)                                              |
| PR          | Label 3         | Blood Pressure (mm Hg)                                                     |
| SK          | Label 4         | Blood Work Result-2 (mm)                                                   |
| TS          | Label5          | Blood Work Result-3 (mu U/ml)                                              |
| M11         | Label 6         | Body mass index (weight in kg/(height in m)^2                              |
| BD2         | Label 7         | Blood Work Result-4 (mu U/ml)                                              |
| Age         | Label 8         | patients age (years)                                                       |
| Insurance   | N/A             | If a patient holds a valid insurance card                                  |
| Sepsis      | Target Label    | Positive: if a patient in ICU will develop sepsis, and Negative: otherwise |

Missing Attribute Values: Yes

## Project Processes

Build an API integrating an ML model using FastAPI.

1.  Build an ML model to predict the [Sepsis](https://www.kaggle.com/datasets/chaunguynnghunh/sepsis?select=README.md).

2.  Build an API using Fast API to embed the ML model built.

3.  Deploy API in Hugging Face

## Setup

Install the required packages to be able to run the evaluation locally.

You need to have [`Python 3`](https://www.python.org/) on your system (**a Python version lower than 3.10**). Then you can clone this repo and being at the repo's `root :: repository_name> ...` follow the steps below:

- Windows:

        python -m venv venv; venv\Scripts\activate; python -m pip install -q --upgrade pip; python -m pip install -qr requirements.txt

- Linux & MacOs:
        python3 -m venv venv; source venv/bin/activate; python -m pip install -q --upgrade pip; python -m pip install -qr requirements.txt

They both have long command-lines which have the same structure, they pipe multiple commands using the symbol `;` but you may manually execute them one after another.

1. **Create the Python's virtual environment** that isolates the required libraries of the project to avoid conflicts;
2. **Activate the Python's virtual environment** so that the Python kernel & libraries will be those of the isolated environment;
3. **Upgrade Pip, the installed libraries/packages manager** to have the up-to-date version that will work correctly;
4. **Install the required libraries/packages** listed in the `requirements.txt` file so that it will be allow to import them into the python's scripts and notebooks without any issue.

**NB:** For MacOs users, please install `Xcode` if you have an issue.

## Run FastAPI

- Run the demo apps (being at the repository root):

  FastAPI:

  - Demo

        uvicorn src.main:app --reload

## Summary

| Code | Name                              |                                               Published Article                                                |                                                                Deployed App |
| ---- | --------------------------------- | :------------------------------------------------------------------------------------------------------------: | --------------------------------------------------------------------------: |
| LP6  | Embedding ML in API using FastAPI | [Article](https://medium.com/@mdkumassah/building-a-machine-learning-api-with-fastapi-and-docker-ea8024752b61) | [API with FastAPI](https://quophydzifa-sepsis-prediction-app.hf.space/docs) |

### Note:

1. To be able to see the interface of the deployed app in Hugging Face, click on the 3 dots beside the settings tab and select ‘Embed space’.
2. Click on ‘Direct URL’. When it shows in the browser, add ‘/docs’ to see the interface.
3. Anytime you want to access the API's interface, add "/docs" to the URL.

App Interface

![apishot](src\apishot.png)

## Resources

Here are some ressources you would read to have a good understanding of FastAPI :

- [Tutorial - User Guide](https://fastapi.tiangolo.com/tutorial/)
- [Video - Building a Machine Learning API in 15 Minutes ](https://youtu.be/C82lT9cWQiA)
- [FastAPI for Machine Learning: Live coding an ML web application](https://www.youtube.com/watch?v=_BZGtifh_gw)
- [Video - Deploy ML models with FastAPI, Docker, and Heroku ](https://www.youtube.com/watch?v=h5wLuVDr0oc)
- [FastAPI Tutorial Series](https://www.youtube.com/watch?v=tKL6wEqbyNs&list=PLShTCj6cbon9gK9AbDSxZbas1F6b6C_Mx)
- [Http status codes](https://www.linkedin.com/feed/update/urn:li:activity:7017027658400063488?utm_source=share&utm_medium=member_desktop)

## Author

- Michael D. Kumassah

  [![LinkedIn](https://img.shields.io/badge/LinkedIn-blue)](https://www.linkedin.com/in/kumassahdzifamichael/)
  [![Hugging Face Spaces](https://img.shields.io/badge/Hugging-Face-yellow)](https://huggingface.co/QuophyDzifa)
