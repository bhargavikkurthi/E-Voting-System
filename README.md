## Overview

The E-Voting System is designed to facilitate online elections by allowing users to create elections, cast votes, and monitor election results. Built using Spring Boot, Hibernate, and MySQL, the system provides a secure and efficient way to manage elections with CRUD operations.

---

## Features

* Election Management: Create elections with unique titles.

* Choice Management: Add multiple choices for each election.

* User Management: Register users with unique usernames.

* Voting System: Allow users to cast votes for elections.

* Result Calculation: Retrieve election results, including total votes and the winning candidate.

* Data Persistence: Uses MySQL for data storage.

* REST API Endpoints for seamless integration.

---

## Tech Stack

* Spring Boot 3.0.0

* Hibernate (JPA for ORM)

* MySQL (Database)

* Postman (For API testing)

---

## Flowchart

1. Create Election → 2. Add Choices → 3. Register Voters → 4. Cast Votes → 5. Monitor Results

---

## API Endpoints


### Election Endpoints

| Method       | Endpoint       | Description                          |
| ------------ |:---------------|:-------------------------------------|
| GET          | /get/elections | Retrieves the list of all elections. |
| POST         | /add/election  | Creates a new election.              |


### ElectionChoice Endpoints

| Method       | Endpoint                | Description                                 |
| ------------ |:------------------------|:--------------------------------------------|
| POST         | /add/electionChoice     | Adds a new election choice.                 |
| GET          | /get/electionChoices    | Fetches the list of all election choices.   |
| POST         | /count/election/choices | Retrieves all choices for a given election. |


### User Endpoints

| Method       | Endpoint   | Description                         |
| ------------ |:-----------|:------------------------------------|
| POST         | /add/user  | Creates a new user in the database. |
| GET          | /get/users | Fetches the list of all users.      |


### Vote Endpoints

| Method       | Endpoint              | Description                                       |
| ------------ |:----------------------|:--------------------------------------------------|
| GET          | /get/votes            | Fetches the list of all votes.                    |
| POST         | /add/vote             | Registers a new vote in the database.             |
| GET          | /count/votes          | Fetches the total count of votes.                 |
| POST         | /count/election/votes | Returns the count of total votes for an election. |


### Results Endpoints

| Method       | Endpoint         | Description                                   |
| ------------ |:-----------------|:----------------------------------------------|
| POST         | /winner/election | Retrieves the winning choice for an election. |
