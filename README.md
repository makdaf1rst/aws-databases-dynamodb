<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Load Data into DynamoDB

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-databases-dynamodb)

**Author:** saqibh49@gmail.com  
**Email:** saqibh49@gmail.com

---

## Load Data into a DynamoDB Table

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-databases-dynamodb_b481c730)

---

## Introducing Today's Project!

### What is Amazon DynamoDB?

Amazon DynamoDB is a fully managed NoSQL database, and it’s useful because it’s extremely fast, automatically scales, and doesn’t require you to manage servers or infrastructure.

### How I used Amazon DynamoDB in this project

In today's project, I used Amazon DynamoDB to create tables, add data via the console and AWS CLI, and then look through the new data using the cinsole. 

### One thing I didn't expect in this project was...

One thing I didn't expect in this project is how different non-relational databases are compared to relational ones. The concept of a table without rows and columns is hard to comprehend, but once I got into it, it became clear how Dynamo stores data differently. 

### This project took me...

This project took me about 40 minutes. 

---

## Create a DynamoDB table

DynamoDB tables organises data using items and attributes. Essentially, instead of a table with columns and rows, DynamoDB basically keeps all the data in lists - for example, one list might be called Nikko (item) and all the items in the list are ProjectsCompleted - 4 (attribute). 

An attribute is basically something that describes an item. For example, in this case, the attribute is ProjectsComplete, because it describes the number of projects completed by Nikko. 

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-databases-dynamodb_a3cefee0)

---

## Read and Write Capacity

Read capacity units (RCUs) and write capacity units (WCUs) are basically engines in DynamoDB that handle tasks like reading, editing, and creating. 1 read capacity unit (1 engine) can perform 2 reads per second, and 1 write capacity unit (1 engine) can perform 1 write action per second. 

Amazon DynamoDB's Free Tier covers 25gb of data, 25 read capacity units and 25 write capacity units. I turned off auto scaling because I don't want DynamoDB to automatically create more than 25 read or write capacity units since that will be a charge. 

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-databases-dynamodb_ef47dd8f)

---

## Using CLI and CloudShell

AWS CloudShell is a terminal built right into the management console that is already connected to AWS. 

AWS CLI is software that lets engineers manage resources within AWS with commands in the terminal instead of with clicks and navigating through the console. 

I ran a CLI command in AWS CloudShell that created 4 new tables, each different items including, partition keys, attributes, and sort keys. 

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-databases-dynamodb_81e0258b)

---

## Loading Data with CLI

I ran a CLI command in AWS CloudShell that told DynamoDB that some data need be uploaded to tables and that the data was stored within specific files. 

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-databases-dynamodb_791c600b)

---

## Observing Item Attributes

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-databases-dynamodb_b481c731)

I checked a ContentCatalog item, which had the following attributes: 
- cat Authors
- ContentType
- Difficulty
- Price
- ProjectCategory
- Published
- Title
- URL

I checked another ContentCatalog item, which had a different set of attributes: 
- ContentType
- Price
- Services
- Title
- URL
- VideoType

---

## Benefits of DynamoDB

A benefit of DynamoDB over relational databases is flexibility, because each item in DynamoDB can have different attributes, whereas in a relational database, each item has to have the same column headers. 

Another benefit over relational databases is speed, because DynamoDB can use autoscaling, so when more traffic is neeeded, it can ramp up it's number of read and write capacity units to meet demand. 

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-databases-dynamodb_b481c730)

---

---
