# APPOINTMENT-SCHEDULER-USING-ALEXA

## Introduction

Step into the world of seamless healthcare management with our cutting-edge Hospital Appointment Scheduler using Alexa skill! Embrace the future of healthcare as you effortlessly book appointments with renowned doctors at XYZ Hospital, all at your command through any Alexa-enabled device. With this skill, you hold the power to manage your health with ease, making the entire appointment booking process a breeze while ensuring you receive the best medical care possible.

## Problem Statement

The primary goal of the Appointment Scheduler using Alexa skill is to streamline the process of scheduling doctor appointments for patients. The skill aims to provide a seamless and user-friendly interface that allows patients to register, verify their identity, and schedule appointments with their preferred doctors based on availability.

## Solution Overview

The Appointment Scheduler skill is built using the Alexa Skills Kit (ASK) and integrates with AWS Lambda for serverless execution. It leverages AWS DynamoDB for storing patient and doctor information, Google Calendar API for doctor availability, and Amazon Simple Email Service (SES) for email notifications.

Here's an overview of the key components of the solution:

1. *User Registration and Verification*: New patients can register by providing their information, including full name, age, gender, date of birth (DOB), father's name, and email. The skill sends a verification email to the provided email address for identity confirmation.

2. *Returning Patients*: Returning patients can log in using their patient ID. If they forget their patient ID, they can verify their identity by providing their father's name.

3. *Doctor Availability Checking*: The skill uses the Google Calendar API to check the availability of doctors for a specified specialization, date, and time. Patients can search for available doctors and choose from the list.

4. *Appointment Booking*: Patients can book appointments with their chosen doctor based on availability. The skill reserves the appointment slot in the doctor's Google Calendar and sends a confirmation email to the patient.

5. *Voice-Based Doctor Recommendations*: Implement a feature that allows Alexa to recommend doctors based on the patient's symptoms or medical conditions. Users can ask Alexa for suggestions, and the skill can provide a list of doctors specializing in relevant fields.

6. *Voice Authentication*: Integrate voice authentication technology to improve security during the registration and login process. This can enhance the skill's ability to verify the identity of patients securely.

7. *Email Notifications*: The skill uses Amazon SES to send verification emails to new patients and confirmation emails for scheduled appointments.

8. *Insurance Information Integration*: Enable the skill to retrieve and store insurance information for patients. This can help streamline billing and insurance processing.

## Tech Stack

The Hospital Appointment Scheduler skill is built using the following technologies:

- **Alexa Skills Kit (ASK)**: A collection of APIs and tools for building voice-driven experiences.
- **AWS Lambda**: A serverless compute service for running code in response to Alexa requests.
- **AWS DynamoDB**: A NoSQL database service for storing patient and doctor information.
- **Google Calendar API**: An API for managing Google Calendar events and availability.
- **Amazon Simple Email Service (SES)**: A service for sending emails to users.

## Work Flow




## Skill Features

### User Registration and Verification

- New patients can register by providing their full name, age, gender, DOB, father's name, and email.
- The skill sends a verification email to the provided email address for identity confirmation.
- After confirmation, The details of patient are stored in the DynamoDB in the form of table.
- Returning patients can log in using their patient ID or if they forgot their patiend ID they can verify their identity using their father's name.
  
### Doctor Availability Checking

- Patients can search for available doctors based on a specified specialization, date, and time.
- The details of the doctors are retrieved from the DynamoDB table of doctors_details.
- The skill uses the Google Calendar API to check the availability of doctors for the specified time slot.

### Appointment Booking

- Patients can schedule appointments with their chosen doctor based on availability.
- The skill reserves the appointment slot in the doctor's Google Calendar.

### Voice-Based Doctor Recommendations

- Alexa can provide doctor recommendations based on the patient's symptoms or medical conditions.
- Users can ask Alexa for suggestions, and the skill will offer a list of doctors specializing in relevant fields.

### Voice Authentication

- The skill can use voice authentication technology for secure user registration and login.

### Email Notifications

- The skill sends verification emails to new patients for identity confirmation.
- Confirmation emails for scheduled appointments are sent to patients' registered email addresses.

## Lambda Function Code

  The Lambda function for the Appointment Scheduler skill is responsible for handling user requests and interacting with the backend services. It is written in Python and integrated with the ASK SDK for Alexa interactions. The code is structured into several intent handlers to handle different user intents, such as registration, login, appointment booking, doctor recommendations, and more.

*Code Link:* https://github.com/AkshayaAdabala/APPOINTMENT-SCHEDULER-USING-ALEXA/blob/main/lambda_function.py 
