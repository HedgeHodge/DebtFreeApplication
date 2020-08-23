* [Background](#background)
* [Overview](#overview)
* [Functionality](#functionality)
* [Deployment](#deployment)
* [Built With](#built-with)
* [Authors](#authors)
* [User Stories](#user-stories)
* [Use Cases](#use-cases)
* [UML Diagram](#uml-diagram)
* [Requirements](#requirements)

# Debt Free Cloud Application

This project is being worked on as part of my final project for the Microsoft-sponsored MSSA Cloud Application Developer cohort hosted by Embry-Riddle Aeronautical University.

## Background

Debt is something many of us live with and often times we don’t see a way to get out of it. The reality is, if we don’t do something about it, it usually piles up until we have no choice but to confront it. Growing up, I wasn’t taught good money management skills and as a result, I let myself get into far too much debt for my own good. I came across the idea of the Debt Snowball, which is the concept that you list your debts smallest to largest and you tackle the smallest one first. This way, as you pay off each small debt, you gain a boost of confidence as you knock them out one by one. The bonus to this is that you also take out a monthly payment that can be added onto your payment for the next debt, hence “The Debt Snowball”. 

## Overview

This application will provide a simple and functional UI that gives you a snapshot of your debts and allows you to work on the next smallest debt one-at-a-time. While I want this application to provide a good bit of functionality, my main focus is on providing motivation to continue making payments towards your debts.

## Functionality

With this application, you will have the ability to register using Email and Password, Google Authentication, or Apple Authentication. After signing in for the first time, you will be presented with a page to enter all of your debts. After you finish entering all your debts, you will arrive at the main page. The main page will consist mostly of a Donut chart to view all debts, a simple list view of the selected debt, and a plus button to add a payment.

## Deployment

This project will be deployed on the Azure platform.

## Built With

* [ASP.NET Core MVC] - The web framework used
* [SQL Server] - Database

## Authors

* **Tyler Hodges**

--------------------------------------------------------------------------------------

## User Stories

*1.*
  __As a__ person who has debt

  __I want__ to payoff my debt

  __So that__ I can become debt-free
  
*2.*
  __As a__ parent

  __I want__ get control of my finances

  __So that__ I can teach my children how to deal with their finances

## Use Cases

__Given__ I am registered 
__When__ I enter the correct credentials
__Then__ I should be authenticated

__Given__ I am not signed up
__When__ I register with my credentials
__Then__ I should have the ability to authenticate

__Given__ I have a $1,000 debt
__When__ I make a payment for $500 
__Then__ I should now have a $500 debt

__Given__ I have a $1,000 debt
__When__ .025% interest accrues
__Then__ I should now have a $1,025 debt

__Given__ I am trying to log in to the website 
__When__ I enter incorrect credentials
__Then__ I should not be authenticated

__Given__ I have a $1,000 debt
__When__ I make a payment for $1,050 on the debt 
__Then__ I should have a $0 debt

## UML Diagram

![Image of UML Diagram](https://github.com/HedgeHodge/DebtFreeApplication/blob/master/UMLDiagram.png)

## Requirements

| no. | Description | Test Method |
|-----|-------------|-------------|
|  1  |the system shall restrict access to authenticated users|Test|
| 1.1 |the application shall present a login screen to the user|Inspection|
| 1.1.1 |the login window shall present a red error if the user enters an incorrect login|Inspection|
| 1.1.2 |the application shall direct user to the next page if login is successful|Inspection|
| 1.2 | the system shall present a register screen to the user|Inspection|
| 1.2.1 |the register window shall present a red error if the user enters an invalid email or password|Inspection|
| 1.2.2 |the register window shall direct user to the next page if registration is successful|Inspection|
|  2  |the user shall be able to add debts|Demonstration|
| 2.1 |the application shall present an add debt screen after initial registration|Inspection|
| 2.1.1 |the system shall present an input area for inital debt entry|Inspection|
| 2.2.1 |the system shall reject non-numerical inputs for debt totals|Test|
|  3  |the user shall be able to add payments to debts|Demonstration|
| 3.1 |the application shall have a button to enable addition of payments|Inspection|
| 3.1.1 |the application shall present a popup to input amount of payment|Inspection|
| 3.2.1 |the application shall reject non-numerical inputs for payments|Test|
|  4  |the user shall be able to adjust debt total based on accrued interest|Demonstration|
| 4.1 |the application shall present a button to add interest charges|Inspection|
| 4.1.1 |the application shall reject non-numerical inputs for interest charges|Test| 
