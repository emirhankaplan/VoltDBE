#   VoltDB

This repository contains SQL scripts to create and populate a `SUBSCRIBER` table, a stored procedure to select all subscribers, and Docker commands to manage your database container.

## Table Creation and Data Insertion

Run the following SQL commands to create the `SUBSCRIBER` table and insert sample data:

```sql
CREATE TABLE SUBSCRIBER(
    SUBSC_ID INTEGER,
    SUBSC_NAME VARCHAR(100),
    SUBSC_SURNAME VARCHAR(100),
    MSISDN VARCHAR(100),
    TARIFF_ID INTEGER,
    START_DATE TIMESTAMP
);

INSERT INTO SUBSCRIBER (SUBSC_ID, SUBSC_NAME, SUBSC_SURNAME, MSISDN, TARIFF_ID, START_DATE) 
VALUES (1, 'Johnathan', 'Doe', '1122334455', 201, '2024-07-28 09:30:00');

INSERT INTO SUBSCRIBER (SUBSC_ID, SUBSC_NAME, SUBSC_SURNAME, MSISDN, TARIFF_ID, START_DATE) 
VALUES (2, 'Jane', 'Williams', '9988776655', 202, '2024-07-28 10:15:00');

INSERT INTO SUBSCRIBER (SUBSC_ID, SUBSC_NAME, SUBSC_SURNAME, MSISDN, TARIFF_ID, START_DATE) 
VALUES (3, 'Alicia', 'Johnson', '5566778899', 203, '2024-07-28 11:00:00');

INSERT INTO SUBSCRIBER (SUBSC_ID, SUBSC_NAME, SUBSC_SURNAME, MSISDN, TARIFF_ID, START_DATE) 
VALUES (4, 'Robert', 'Brown', '4455667788', 204, '2024-07-28 11:45:00');

INSERT INTO SUBSCRIBER (SUBSC_ID, SUBSC_NAME, SUBSC_SURNAME, MSISDN, TARIFF_ID, START_DATE) 
VALUES (5, 'Charles', 'Davison', '3344556677', 205, '2024-07-28 12:30:00');

```
Stored Procedure
Create a stored procedure to select all subscribers:
```
CREATE PROCEDURE selectAllSubscribers AS 
SELECT * FROM SUBSCRIBER;
```

Docker Commands
To list running Docker containers and find out the port on which your database container is running, use the following command
docker ps
This command will display a list of all running Docker containers along with their ports.

Usage
Run the SQL scripts to create the SUBSCRIBER table and insert data.
Create the stored procedure using the provided SQL command.
Use the docker ps command to find your database container and its port.
Connect to your database and run the selectAllSubscribers procedure to retrieve all subscriber data.
Feel free to customize the SQL scripts and Docker commands as per your requirements.
