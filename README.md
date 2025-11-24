# Simple Hotel Management System (Hotel VIT Bhopal)

This is a basic, console-based hotel room management system implemented in Python. It allows users to view room availability, book a room, and check out a guest.

# Features

* **Display Room Status:** View a detailed list of all rooms, their type, price, current status (Available/Booked), and the guest name (if booked).
* **Book a Room:** Allows booking an available room by entering the room number and guest name.
* **Check Out a Room:** Frees up a booked room and provides a basic charge notification.
* **Simple Menu Interface:** An interactive menu for easy navigation.

#How to Run

1.  **Save the Code:** Save the provided Python code into a file named `hotel_management.py`.
2.  **Run:** Open your terminal or command prompt, navigate to the directory where you saved the file, and run the script:

    ```
    python hotel_management.py
    ```

3.  **Interact:** Follow the on-screen menu prompts to perform actions (1, 2, 3, or 4 to exit).

##  Code Structure

### 1. Data Initialization

The system starts with a list of room dictionaries containing initial room data.

* `rooms_data`: A list of dictionaries, where each dictionary represents a room with keys like `"number"`, `"type"`, `"price"`, `"is_available"`, and `"guest"`.
* `Hotel_VIT_Bhopal`: A simple string variable holding the hotel name/context.

```python
rooms_data = [...] # (Initial room data)
Hotel_VIT_Bhopal = "hotel for firstyears "
