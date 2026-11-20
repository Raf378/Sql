# Car Rental Booking Database

Create a simple relational database for a car rental system. The goal is to practice creating tables, relationships, primary keys, foreign keys, basic constraints, and SQL queries.

## 1. Database Tables

* **customers**
  * `customer_id`
  * `first_name`
  * `last_name`
  * `email`
  * `driver_license`
  * `phone`

* **locations**
  * `location_id`
  * `city`
  * `address`
  * `phone`

* **cars**
  * `car_id`
  * `location_id`
  * `brand_model`
  * `license_plate`

* **rentals**
  * `rental_id`
  * `customer_id`
  * `car_id`
  * `start_date`
  * `end_date`

## 2. Relationships

* A location can have many cars.
* Each car belongs to one location.
* A customer can make many rentals.
* A car can be included in many rentals.
* Each rental belongs to one customer.
* Each rental is for one car.
* The relationships between tables must be implemented using foreign keys.

## 3. Required Constraints

* Every table must have a `PRIMARY KEY`.
* Customer `email` must be `UNIQUE` and `NOT NULL`.
* Customer `driver_license` must be `UNIQUE` and `NOT NULL`.
* Car `license_plate` must be `UNIQUE` and `NOT NULL`.
* `brand_model`, `city`, `address`, `first_name`, and `last_name` must be `NOT NULL`.
* Rental `end_date` must be greater than or equal to `start_date`.
* All foreign keys must reference the appropriate tables.

## 4. Sample Data

* 2–5 customers
* 2–3 locations
* 2–5 cars
* 2–6 rentals

## 5. Required SQL Queries

* Display all customers.
* Display all cars with their locations.
* Display all rentals with customer names, car models, and rental dates.
* Display all rentals for a selected customer.
* Display all rentals for a selected car.
* Count how many rentals each customer has.
* Display cars located in a specific city.
* Display rentals ordered by start date.