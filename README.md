# Neighbourhood Collaboration Site

We are building a neighbourhood collaboration site and we want to make a system to keep track of people, houses, and addresses of those houses.

## SQL vs NoSQL

Our data will be structured with a predefined schema, therefore we will use an SQL database. SQL databases are relational which will allows us to identify and access data in relation to another piece of data in the database.

## Schema

Table 1 - Owners:

| Owner Name  | Age |
| ----------- | --- |
| John Smith  | 45  |
| Amy Brown   | 36  |
| Jenny Green | 28  |
| Tom Hanks   | 54  |

Table 2 - Houses:

| Name        | Street Address      | No. of people in household |
| ----------- | ------------------- | -------------------------- |
| John Smith  | 48 Barnaby Street   | 4                          |
| Amy Brown   | 12 Exeter Road      | 2                          |
| Jenny Green | 23 Castlehill Way   | 1                          |
| Tom Hanks   | 8 Coronation Street | 6                          |

Table 3 - Addresses:

| Street Address      | Postcode |
| ------------------- | -------- |
| 48 Barnaby Street   | NW1 7PO  |
| 12 Exeter Road      | NW1 6DT  |
| 23 Castlehill Way   | NW2 3FT  |
| 8 Coronation Street | NW1 5PR  |

## API Requests

### Our API should be capable of handling the following requests:

- **GET**
- **POST**
- **PATCH** (update no. of people/age)
- **PUT** (replace an entry e.g. new owner of house)
- **DELETE**

## Routes List

| **Path**        | **HTTP Verb** | **Action** |
| --------------- | ------------- | ---------- |
| /owners/        | GET           | index      |
| /owners         | POST          | create     |
| /owners/address | GET           | show       |
| /owners/:id     | GET           | show       |
| /owners/:id     | PATCH/PUT     | update     |
| /owners/:id     | DELETE        | destroy    |

## Responses

GET Requests

- **/owners/** will return a JSON object containing owner name and age.

- **/owners/address** will return a JSON object containing the full address of each owner.

- **/owners/:id** will return a JSON object containing the details of a specific owner.

POST Requests

- **/owners/** will add a new entry to the owners table in the API database.

PATCH/PUT Requests

- **/owners/:id** will ammend the details of a specific owner (PATCH) or replace an existing entry with a completely different one(PUT).

DELETE Requests

- **/owners/:id** will remove a specific entry from the API database.
