# AMA Node Developer Assessment

Thank you so much for considering the AMA Development Team for your next career opportunity!

In lieu of an extensive live-coding interview, we invite you to complete this take-home assessment. It is meant to evaluate some basic skills that are required to be successful as a developer at the American Marketing Association.

We're aware of the time commitment required for this process and want to respect your time. This assessment can be satisfactorily completed within a few hours. You also have 1 full week to complete it so pick a time that works best for you.

Once complete, post your code in a Github repository and send the link to your recruiter. If you would rather keep the repo private, please add @aaroneaton as a collaborator.

If you run into any trouble completing this assignment, please contact your recruiter so we can help you out.

Good luck!

## Prerequisites
- An active AWS account (everything in this assessment fits within the free tier)
- AWS CLI configured on your local machine (try `aws iam get-user` to quickly check this)
- Some experience with Typescript, or expert experience with vanilla Javascript
- A passing familiarity with AWS CDK (or an interest in learning the basics)
- Node v16+ installed

## The Problem
We have data in Google Analytics that can tell us the number of impressions on a certain page as well as the advertising budget spent acquiring those impressions. We need to get this information into our own database for further processing.

Your task is to create a GraphQL API which can receive the impression/budget data, save it to our database and allow it to be queried. Due to some constraints in our system, the data received through the API should pass through a message queue or broker before being saved in the database.

Sample data can be found in "Advertising_Budget.csv" at the root of this project.

## Getting Started
1. Clone this repo to your local machine
2. Confirm that your AWS CLI can connect to your AWS account
3. Run `npm install` to install all of the required packages
4. Run `npm start` to create the initial infrastructure in AWS and start local development

## Acceptance Criteria
1. It has a GraphQL mutation that receives the impressions and budget for a single month
2. The data received from that mutation passes through a message queue or broker (SQS, SNS, Eventbridge. Your choice.)
3. Each entry is saved to a DynamoDB table
4. It has a GraphQL query that returns the impressions and budget for a given month
5. It has a GraphQL query that returns the impressions and budget for all months

## Helpful Hints
The AMA Development Team makes use of a library called [Serverless Stack](https://sst.dev/). It provides additional constructs on top of AWS CDK to make serverless development a breeze! This project is built with the minimal SST starter. Please take a look at [SST's documentation](https://docs.sst.dev/) to find the constructs you need to build out this assessment.

Never done a take-home assessment before? No worries! Nervous? Don't be! We're not looking for a perfectly executed solution with 100% test coverage. We're simply looking to evaluate some basic skills. [Here](https://betterprogramming.pub/got-a-take-home-coding-assignment-here-is-how-to-prepare-for-it-bd04c2f5d972) are some tips to make this a success.

Don't hesitate to reach out if you get stuck on an issue.

## Credits
The dataset originated from [Kaggle](https://www.kaggle.com/datasets/arnabdata/advertising-budget).