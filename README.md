# APPOINTMENT-SCHEDULER-USING-ALEXA

## Introduction

Step into the world of seamless healthcare management with our cutting-edge Hospital Appointment Scheduler using Alexa skill! Embrace the future of healthcare as you effortlessly book appointments with renowned doctors at XYZ Hospital, all at your command through any Alexa-enabled device. With this skill, you hold the power to manage your health with ease, making the entire appointment booking process a breeze while ensuring you receive the best medical care possible.

## Problem Statement

The primary goal of the Appointment Scheduler using Alexa skill is to streamline the process of scheduling doctor appointments for patients. The skill aims to provide a seamless and user-friendly interface that allows patients to register, verify their identity, and schedule appointments with their preferred doctors based on availability.

## Solution Overview

The Appointment Scheduler skill is built using the Alexa Skills Kit (ASK) and integrates with AWS Lambda for serverless execution. It leverages AWS DynamoDB for storing patient and doctor information, Google Calendar API for doctor availability, and Amazon Simple Email Service (SES) for email notifications.

Here's an overview of the key components of the solution:

1. *User Registration and Verification*: New patients can register by providing their information, including full name, age, gender, date of birth (DOB), father's name, and email. The skill sends a verification email to the provided email address for identity confirmation.
