# Architect and Build an End-to-End AWS Web Application from Scratch

## Tutorial Credit
This GitHub repository and README.md page are based on a tutorial by Tiny Technical Tutorials. The tutorial video that inspired this repository can be found on [Tiny Technical Tutorials YouTube Channel](https://www.youtube.com/@TinyTechnicalTutorials). Please visit the channel and consider subscribing for more great tutorials.

```{raw} html
<iframe width="560" height="315" src="https://www.youtube.com/embed/7m_q1ldzw0U?si=QHTM9bY-n5fG34Yh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```
## Introduction
Let me tell you a story…

Hi there and welcome to the channel. Let's start off this video with a story. Once upon a time when I first started learning AWS, I learned bits and pieces of it. Some of the core services, I could find my way around the AWS console. I could do things like create a new EC2 instance or create an S3 bucket and upload something to it, and I felt like my learning was going along pretty well. But then one day, I was telling some friends about AWS and how I was learning a new way to do development, and one of them said, "Send me a link to something because I want to check out your handiwork," which made me stammer a little bit about that. Because it made me realize two things: one, I hadn't actually built anything that I could share with the outside world, and two, and more importantly, I didn't actually know how to build something because I wasn't able to put all the services together into an actual application. I knew what the puzzle pieces were, in other words, the different AWS services I had been learning about, but I wasn't able to put them together into an actual usable thing. And if you're feeling the same way, you've come to the right place.

## Overview of the Services and Application
In this video, we'll be using five AWS services to build an end-to-end web application from scratch. And yes, you can even share it with your friends when you're done if you'd like. Let me show you the working version.

### The Power of Math
Now admittedly, this is a super simple application, but it ties together all of the main components that you would need to build a much larger real-world application. This just takes in two different numbers, so we have a base number (let's say 2) and then an exponent (we'll go with 5), and it's going to return the result: the base to the power of the exponent. If we click on "Calculate," the result is 32. You'll see that we get that in the popup. It's also being saved to a DynamoDB table on the backend if you wanted to do something with it down the line.

## Prerequisites
Before you get started, here's what you'll need to follow along with this tutorial:
- A text editor (e.g., Notepad++, Visual Studio Code, or your favorite editor).
- An AWS account and access to the AWS console. If you don't have one already, you can set it up using the link above and below.
- Basic knowledge of AWS. While this video won't be a deep dive into any specific AWS service, it's helpful to have some basic understanding of AWS concepts.

## Building the Web Application
### Creating and Hosting a Web Page
To create and host a web page for our web application, we'll use AWS Amplify. Amplify allows us to build and host websites easily. For this tutorial, we'll create a simple HTML page and use Amplify to deploy and host it.

Here's a quick overview of the steps:
1. Create a new HTML file locally (e.g., index.html).
2. Write the HTML code for your web page (You can find the code in this repository under `index-original.html`).
3. Zip the HTML file.
4. Deploy the web page using AWS Amplify.

### Doing Math Calculations
To implement the math functionality of our web application, we'll use an AWS Lambda function. Lambda is a serverless compute service that allows you to run code in response to various triggers. In this case, we'll use it to perform mathematical calculations.

Here's what we'll do:
1. Create a Python Lambda function from scratch.
2. Write Python code to perform the math calculation.
3. Test the Lambda function to ensure it's working as expected.

### Invoking the Lambda Function
Next, we need a way to invoke the Lambda function to perform the math calculation. We'll use Amazon API Gateway to create a RESTful API endpoint that can trigger our Lambda function.

Here's the process:
1. Create a REST API using Amazon API Gateway.
2. Add a POST method to the API to trigger the Lambda function.
3. Enable CORS (Cross-Origin Resource Sharing) to allow the API to be called from our web page.
4. Deploy the API.

### Storing Results and Permissions
To store the math results and handle permissions, we'll use Amazon DynamoDB, a NoSQL database service provided by AWS. We'll also set up the necessary permissions for our Lambda function to write data to DynamoDB.

Here's what we'll do:
1. Create a DynamoDB table to store math results.
2. Define an IAM (Identity and Access Management) role to grant permissions to the Lambda function.
3. Modify the Lambda function to write results to DynamoDB.

### Final Touches and Testing
In the final steps, we'll update our web page to make API calls, handle responses, and display the results. We'll also test the entire application to ensure everything is working correctly.

Here's a summary:
1. Update the JavaScript code on our web page to call the API.
2. Handle API responses and display the results on the web page.
3. Test the web application by entering different numbers and checking the results.

## Conclusion
That's it! We've successfully built an end-to-end web application using AWS services. You've learned how to create a web page, implement serverless compute with Lambda, create RESTful APIs with API Gateway, and use DynamoDB for data storage. You can take this knowledge and expand it to build more complex applications on AWS.

If you found this tutorial helpful, please consider giving it a star on GitHub and subscribing to my YouTube channel for more AWS tutorials and tech content. Thank you for watching, and I'll see you in the next one!
