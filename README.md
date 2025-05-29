# Flight-Fare-Prediction
 
This Flask application predicts the price of a flight ticket based on various user inputs such as departure time, arrival time, airline, source, and destination. Here's a breakdown of the steps performed:

 1. Import Libraries
Essential libraries such as Flask, pandas, and pickle are imported for web development, data processing, and loading the trained model.

2. Load the Trained Model 
A pre-trained Random Forest model (flight_rf.pkl) is loaded using pickle.

 3. Define Home Route
The home route renders an HTML page (home.html) that contains a form for the user to input flight details.

4. Handle Form Submission
The /predict route processes form inputs when the user submits the form.

5. Extract and Process Inputs
Date & Time values (departure & arrival) are parsed and split into components like day, month, hour, and minute.

Flight Duration is calculated from the difference between departure and arrival times.

Categorical Values like Airline, Source, and Destination are one-hot encoded manually.

Total Stops is directly parsed as an integer.

 6. Feature Vector Creation
All processed values are collected into a specific order matching the model’s input structure.

7. Make Prediction
The model predicts the flight price based on the input features.

8. Return the Prediction
The predicted price is rounded and displayed back to the user on the HTML page.
