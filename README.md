## International Airfare Price Predictions
Repository for Stat 418 final project

#### DESCRIPTION
Conducting analysis on webscraped data from Norwegian Air Shuttle for various flight itineraries from the US to Europe. Building prediction model to assist with purchasing decisions. Model to be hosted on Amazon EC2 and accessible via Flask API application

#### DATA COLLECTION
Webscrape using Python Requests and BeautifulSoup

#### ACKNOWLEDGEMENTS
All data collected is in adherence to Norwegian Air Shuttle Terms of Use and intended for personal, academic purposes only

</br>

***

</br>

## EC2 Hosting
The predictive model is hosted on Amazon's EC2 and accessible via a Flask API (instructions below)

</br>

## Accessing Flask API
Please follow the steps below to execute the API:

+ To send a request to the API, use a `curl` command like the example below:  
`curl -H "Content-Type: application/json" -X POST -d '{"":"","":"","":"","":"","":"","":"","":""}' "http://localhost:5000/predict_airfare"`  

> The response should look like: `{airfare prediction: }`

</br>

**To reproduce the API:**

+ Download the files in this repository

+ In your terminal, navigate to the **docker** folder directory and run `docker-compose up` to create your local server

+ If created successfully, you should see output lines with `flask_1 | ....` outputs but will *not* be returning a prompt

+ Open up a new terminal and navigate to the same **docker** directory

+ To check the status of the server run:
`curl https://localserver:5000/`  
The response should say: Server is up!

+ To then access model predictions, follow the steps above for *Accessing Flask API*
