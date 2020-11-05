Backend Developer Take Home Test
====

Introduction
----
This test is the simulation test to represent about how and what we do day by day, if you pass this test then we can assume you are ready to join us.

We want you to create online Loket reservation. Loket will have many event at one time, each event will be held on specific location at specific date, also each event will have one or more ticket that can be purchased by customer. 

Your job here is to create database schedule to accomodate storing event data and export functionalities through HTTP API

Constraints and Requirement
----

- One event will have exactly one location
- One location might have one or more event
- One event will have exactly one schedule
- One schedule might start and end at different day
- One event might have more than one ticket type
- One ticket type must have price and quota, if quota is less than 1 then the ticket cannot be purchased
- Customer will be able to make transaction to purchase ticket event
- Customer can purchase ticket event many times
- For each transaction, customer only can purchase ticket within same event
- Within one transaction, customer can purchase more than 1 ticket type, and more than 1 qty per ticket type


Task
----
1. Create Database Schema using RDBMS based on Constraints and Requirements above. You can also use NoSQL like MongoDb if you want to

2. Create Web Service JSON API with these main functionalities, if there is another function is important from your concern you can create it and add the function description on ASSUMPTIONS.md :

Endpoint | Relative Path | Method | Description
--- | --- | --- | ---
Create Event | */event/create* | POST | Endpoint to create new event
Create Location | */location/create* | POST | Endpoint to create new location
Create Ticket | */event/ticket/create* | POST | Endpoint to create new ticket type on one specific event
Get Event | */event/get_info* | GET | Endpoint to retrieve event information, including location data and ticket data
Purchase Ticket | */transaction/purchase* | POST | Endpoint to make a new purchase, customer data is sent via this API
Transcation Detail | */transaction/get_info* | GET | Endpoint to retrieve transaction created using endpoint *Purchase Ticket*

3. Please use UUID for each Id
4. Organized response codes

Assesment
----

1. Development flow, using spec is preferred
2. Clean and Readable code, good in naming class.
3. Versioning API is a must
4. Input validation handling
5. Have consistency in response on each API Endpoint
6. Have coverage test
7. Have linter implementation

Notes
----

- For each endpoint it's up to you to decide which parameter is required and which parameter is optional
- Ignore authentication, all API endpoint must be accessible **without** any authentication.
- Please do the documentation installation step by step in a ***README.md***, assume the reader is very stupid and don't know about your technology you use. So make sure the documentation is very clear, readable, and can be tested smoothly.
- Please document your assumption in a ***ASSUMPTIONS.md*** if you have your own concern about concept what when wrong and what is good usually people do with the module you have use. Or if you have a good idea in Loket test business you can explain in this document.
- Dump your database schemas, and include it in git repository. Or you can use migration script and seeder. Make sure you attach it on your documentation.
- After you finish with your assignment, you can share your git repository url and send it to HRD
- If you can't complete your assignment in time and need extra day to complete, send your request to HRD, 
explaining your condition and state how much extra days you need. The duration itself took 1 week.

### HAVE FUN & SEE YOU AT INTERVIEW
