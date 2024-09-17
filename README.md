Airlines Database
This README.md provides an overview of the Airlines database schema, including details about tables, attributes, and their relationships. The database is designed to manage information related to airports, passengers, pilots, flights, and tickets.

Database Schema
The Airlines database includes the following tables:

AIRPORT
PASSENGER
PILOT
FLIGHT
TICKET
Tables Overview
1. AIRPORT Table
Attributes:

A_NAME (VARCHAR): Name of the airport.
CITY (VARCHAR): City where the airport is located.
COUNTRY (VARCHAR): Country where the airport is located.
CODE (VARCHAR): Primary Key, unique airport code.
Description: The AIRPORT table contains information about airports.

Independent Entity: The AIRPORT table is an independent entity as it does not rely on any other table.

2. PASSENGER Table
Attributes:

P_ID (INT): Primary Key, unique passenger ID.
NAME (VARCHAR): Name of the passenger.
NATIONALITY (VARCHAR): Nationality of the passenger.
PASSPORT_NO (VARCHAR): Passport number of the passenger.
LANGUAGE_WEIGHT (INT): Language proficiency weight.
Description: The PASSENGER table holds details about passengers.

Independent Entity: The PASSENGER table is an independent entity.

3. PILOT Table
Attributes:

PILOT_ID (INT): Primary Key, unique pilot ID.
NAME (VARCHAR): Name of the pilot.
LICENSE_NO (VARCHAR): Pilot’s license number.
AIRLINE_ID (VARCHAR): Identifier for the airline the pilot is associated with.
MARITAL_STATUS (VARCHAR): Marital status of the pilot.
SALARY (DECIMAL): Salary of the pilot.
DEPT (VARCHAR): Department the pilot is assigned to.
Description: The PILOT table includes information about pilots.

Independent Entity: The PILOT table is an independent entity.

4. FLIGHT Table
Attributes:

FLIGHT_NO (VARCHAR): Primary Key, unique flight number.
DEPARTURE_AIRPORT (VARCHAR): Foreign Key, references the AIRPORT table.
ARRIVAL_TIME (DATETIME): Flight arrival time.
TAKEOFF_TIME (DATETIME): Flight takeoff time.
FLIGHT_TYPE (VARCHAR): Type of flight (e.g., International).
Description: The FLIGHT table holds information about flights, including departure and arrival details.

Dependent Entity:

DEPARTURE_AIRPORT references the AIRPORT table, linking flights to their departure airports.
5. TICKET Table
Attributes:

T_NUM (INT): Primary Key, unique ticket number.
PASSENGER_ID (INT): Foreign Key, references the PASSENGER table.
SEAT_NUM (VARCHAR): Seat number assigned to the passenger.
CLASS (VARCHAR): Class of the ticket (e.g., Economy, Business).
PRICE (DECIMAL): Price of the ticket.
BOOKING_TIME (DATETIME): Time when the ticket was booked.
Description: The TICKET table records details about tickets purchased by passengers.

Dependent Entity:

PASSENGER_ID references the PASSENGER table, linking tickets to the passengers who purchased them.
