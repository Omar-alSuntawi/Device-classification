# Devices Price Classification System

## Technologies Used:

* Visual Studio Code
* Python, Flask   
* Spring Boot 3.2.5, Spring Web, H2 Database, JPA Repository
* Sklearn Machine Learning

## Project Requirements:
* Java 22 JDK
* Maven 3.9.6
* Flask
* Sklearn

## Structure Description:
  ### Python Folder -->
  1. Omar_alSuntawi.ipynb -->
  Python Notebook in which several ML classifiers "Random Forest, KNN, Naive Bayes, Decision Trees, Logistic Regression, Support Vector Machine" were fitted to "train.csv" file after data preprocessing steps and EDA. In addition, performing hyper-parameters tuning using GridSearch to find the best tuning for each model. Finally, application of different assessments and metrics such as "Accuracy, Precision, Recall, F1 Score, and more".

  2. LR_best.pkl --> Pickle file in which the best model with the best hypertuning of parameters is selected and ready to be loaded on any test data.

  3. app.py --> With an endpoint /predict POST that takes device information without the price_range and return the device updated with its prediction.

  4. test.py --> Testing the endpoint by manual injection of sample devices from "test.csv" file.

  ### device-api Folder -->
  1. pom.xml --> XML Configuration file for Spring application that contains the dependencies.

  2. src/test/DeviceApiApplicationTests.java --> Contains a test testOutput10SamplesFromDeviceTable that prints the first 10 samples from the database.

  3. src/main/resources --> Contains "application.properties" file in which configuration of database connection is established, "test.csv" for testing reading from CSV and insertion to the database.

  4. src/main/java/omar/deviceapi/ -->
    1. DeviceApiApplication.java --> which is the first file to run (main class)
    2. model/Device.java --> Declaration of Device entity with set and get functionss for each variable.
    3. repository/DeviceRepository.java --> Extended to the JPA repository which provides functionalies to do with CRUD operations on the database.
    4. controller/DeviceController.java --> Which is the main drive in which handling of web requests (GET,POST) and their routes.
    5. service/DeviceService.java --> In which the logic for the endpoints are defined.
    6. resttemplateconfig/restTemplateConfig.java --> Definition of a bean for RestTemplate module(used to get the response from Python api).

    7. controller/CSVController.java --> A controller class to test reading from test.csv in resources.
    8. service/CSVService.java --> in which the logic for reading CSV from resources is implemented.

## Demo:
* run "app.py" file for Python api which runs on http://localhost:5000
* run from folder src/main/.../deviceapi the following maven command to start "mvn exec:java" this will run on http://localhost:8080
* try different endpoints to get all devices, to add a device, and to save a device 
* send a POST request to it on http://localhost:5000/predict with the device to predict

## Notes and Improvements:
* This project is intended to be submitted as a test for an available "AI Engineer" position.
* Still in need for some work around the endpoints HTTP type (GET,POST)
* User interface