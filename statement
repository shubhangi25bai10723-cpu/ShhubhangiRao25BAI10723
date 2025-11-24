# Statement of Purpose for Hotel Management System

## Project Title
Simple Console-Based Hotel Room Management System

## Author
ShubhangiRao25BAI10723

##  Objective
The primary objective of this Python script is to simulate a **basic hotel reception system**. It allows users to manage room availability, handle guest bookings, and process guest check-outs through a simple, interactive command-line interface.

##  Implementation Details

The system is implemented using **Python** and relies on a list of dictionaries (`rooms_data`) to store and manage the state of each room.

### 1. Data Structure
The core data is stored in the `rooms_data` list. Each room is represented by a dictionary with the following key attributes:
* `"number"`: The unique identifier for the room (e.g., "101").
* `"type"`: The category of the room (e.g., "Standard Non-AC", "Deluxe AC").
* `"price"`: The cost per night (e.g., 1000.00).
* `"is_available"`: A boolean (`True`/`False`) indicating the current booking status.
* `"guest"`: The name of the guest currently occupying the room, or `None` if available.

### 2. Key Functions Implemented

| Function | Role | Logic/Feature |
| :--- | :--- | :--- |
| `display_rooms()` | **Status View** | Prints all room details in a neatly formatted table, clearly distinguishing between **Available** and **Booked** rooms. |
| `book_room()` | **Booking** | Takes user input for **Room Number** and **Guest Name**. Checks if the room exists and is available before updating `is_available` to `False` and setting the `guest` name. |
| `checkout_room()` | **Check-Out/Billing** | Takes user input for **Room Number**. Checks if the room is booked, resets the room state (makes it available, sets `guest` to `None`), and provides a **basic single-night charge** notification. |
| `main_menu()` | **User Interface** | Provides an infinite loop with a menu (1-4) to guide the user and call the appropriate functions. |

## Project Context
This project serves as a practical demonstration of fundamental programming concepts, including:
1.  **List and Dictionary Manipulation:** Managing and updating data within a complex list structure.
2.  **Function Definition:** Modularizing code into reusable functions.
3.  **Conditional Logic:** Using `if/elif/else` statements for decision-making (e.g., checking availability, validating input).
4.  **Input/Output Handling:** Interacting with the user via `input()` and providing formatted feedback via `print()`.

