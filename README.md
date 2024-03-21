# AWS Simple Cloud Project for CS4990 Cloud Computing
## Brief Explanation of Project:

I implemented a web application that allows students at Cal Poly Pomona to book a study room based on input data such as their name, student identification number, number of people a part of the study room, the date as well as the time spans. Since I restricted the web application to be for CPP students only, they have to sign up or login with their credentials in order to access the booking form. Once the student has entered and submitted their booking data, the data is populated on the web page in a table like format. In addition to that the submit button contains a lambda function trigger such that when the input data is submitted, the function is invoked by a rest api to extract the data and store the information to a database in AWS. Below is a diagram showcasing the structure of AWS services that are used within this web application and how I connected them with one another that enable the functionalities. I implemented the project design structure with basic HTML and CSS code. 

<img width="486" alt="image" src="https://github.com/AnnaSoHock/AWS_SimpleCloudProject/assets/81744048/225da387-5ae8-4982-aea2-ed5aca6e18de">

Explanation: The project was hosted via Amplify. In order to specifically extract booking data, I created a lambda function in python format that specifies the parameters as well as establishing the connection to the database with the AWS SDK. In order to invoke the Lambda function within the web application, I created an API Gateway to perform a POST HTTP request through a Rest-API. For the Lambda function to write to the Database, I needed to configure the IAM policies respectively. Then I created a database via DynamoDB that stores all of the data entered from the web application. I enhanced the lambda function and integrated the data to be specifically stored to the user via a unique identifier. Lastly, I integrated the API call code to our source code, so that all services were able to work accordingly with the web application.

## Future functionalities I would like to implement: 
If I had more time to work on this project, I would want to add more features to the webpage to enhance the user experience and interface. The functionalities include features such as a navigation bar, or even provide a real-time booking diagram, so that students know which dates and times have already been reserved. Another feature that I have read about that AWS provides, is the LexBot feature. The LexBot is an integrated Chatbot feature that allows developers to provide real-time support to a user. This chatbot can be modified by the developer in a way that it gives customised answers. It could even be connected with the Database, such that if the user would ask if a certain time slot is free, then it can connect with the Database to give a real-time accurate answer on the status, given the data.

<img width="1290" alt="image" src="https://github.com/AnnaSoHock/AWS_SimpleCloudProject/assets/81744048/53a4b1ab-10f2-498a-8b3f-3959019b81de">

*Video will be published soon*

