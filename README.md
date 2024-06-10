# Story Number Generator

A GitHub action that automatically generates issue numbers for user stories

---

## Prerequisites

#### GitHub Application

A GitHub appication with the correct permissions will be needed. During the action, another action is used to generate a token, this will require the application ID and the application key.

##### Permissions
- Read Access: Organisation secrets
- Read + Write Access: Issues, organisation variables, and pull requests

#### Organisation Variable
- A variable to track and increment the current issue number.

## How It Works

1) Issue Prefix: The action receives an issue prefix as an input.
2) Retrieve Current Issue Number: It retrieves the current issue number from the organisation variable.
3) Generate Story Number: The current issue number is incremented during the script to avoid conflicts as much as possible. The incremented number is then concatenated with the prefix to form the story number.
4) Update Organisation Variable: The incremented issue number is saved back to the organisation variable.
5) Modify Issue Title: The issue title is updated so that the generated story number prefixes the original story title.
