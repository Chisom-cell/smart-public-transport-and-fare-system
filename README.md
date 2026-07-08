# Smart Public Transport & Fare System

An advanced, object-oriented terminal application designed to simulate modern transit networks, manage vehicle seating charts dynamically, and generate graphical business analytics. Built as a Week 3 Full-Stack project for TechRise Cohort 3.

---

## Key Features

* **Object-Oriented Architecture:** Features structural inheritance chains separating Drivers and Passengers from a common `Person` base class, alongside specific Vehicle types (`Bus`, `Minivan`, `Shared Taxi`).
* **Custom Python Decorators:** 
  * `@timer`: Tracks and logs system performance metrics in milliseconds.
  * `@retry`: Automatically catches reservation collisions and retries booking routines safely.
* **Robust Error Handling:** Leverages dedicated custom exceptions (`SeatUnavailableError`, `TripFullError`, `DriverUnavailableError`, `InvalidStopError`) to prevent operational race conditions.
* **Dynamic Demo Mode:** Auto-generates simulated passenger profiles, searches routing paths, and books available seats dynamically until vehicles reach peak capacity.
* **Data Analytics Engine:** Bundles data into Pandas DataFrames and utilizes Matplotlib's non-interactive `Agg` backend to output automated visual reports without blocking execution.

---

## File Structure

```text
smart-public-transport/
│
├── .gitignore
├── README.md
├── requirements.txt
└── smart_public_transport_and_fare_system.py
```

---

## Setup & Installation

### Prerequisites
* Python 3.x installed on your computer.
* A terminal window or PowerShell instance


---

## Sample Performance Metrics

When modules execute, the system outputs live performance analytics to the console:

```text
[TIMER] calculate_fare executed in 0.0412 ms
[RETRY] Attempt 1/3 failed: Seat 12B is unavailable for trip T102
[RETRY] Retrying in 0.5 seconds...
[TIMER] book_seat executed in 502.1480 ms
```
