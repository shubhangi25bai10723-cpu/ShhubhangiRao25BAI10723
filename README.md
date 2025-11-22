# ShhubhangiRao25BAI10723
rooms_data = [{"number": "101", "type": "Standard Non-AC", "price": 1000.00, "is_available": True, "guest": None},
    {"number": "102", "type": "Standard Non-AC", "price": 1000.00, "is_available": True, "guest": None},
    {"number": "201", "type": "Deluxe AC", "price": 2500.00, "is_available": True, "guest": None},
    {"number": "202", "type": "Deluxe AC", "price": 2500.00, "is_available": True, "guest": None},  
    {"number": "301", "type": "Premium AC", "price": 3000.00, "is_available": True, "guest": None},
    {"number": "302", "type": "Premium  AC", "price": 3000.00, "is_available": True, "guest": None},]

Hotel_VIT_Bhopal = "hotel for firstyears "

def display_rooms():
    """Prints the status of all rooms."""
    print(f"\n--- Rooms at {Hotel_VIT_Bhopal} ---")
    print(f"{'Room No.':<10} | {'Type':<20} | {'Price/Night':<15} | {'Status':<12} | {'Guest Name':<20}")
    print("-" * 80)
    for room in rooms_data:
        status = "Available" if room["is_available"] else "Booked"
        guest = room["guest"] if room["guest"] else "N/A"
        print(f"{room['number']:<10} | {room['type']:<20} | ${room['price']:<14.2f} | {status:<12} | {guest:<20}")
    print("-" * 80)
    def book_room():
    """Handles the booking of a room."""
    display_rooms()
    room_num = input("Enter the number of the room you want to book: ").strip()
    guest_name = input("Enter the guest's name: ").strip()

    found = False
    for room in rooms_data:
        if room["number"] == room_num:
            found = True
            if room["is_available"]:
                room["is_available"] = False
                room["guest"] = guest_name
                print(f"\nSUCCESS: Room {room_num} booked for {guest_name}.")
            else:
                print(f"\nERROR: Room {room_num} is already booked.")
            break
    
    if not found:
        print(f"\nERROR: Room number {room_num} not found.")

def checkout_room():
    """Handles checking out a guest and freeing a room."""
    display_rooms()
    room_num = input("Enter the number of the room to check out: ").strip()
    
    found = False
    for room in rooms_data:
        if room["number"] == room_num:
            found = True
            if not room["is_available"]:
                guest_name = room["guest"]
                # just provide a basic price notification.
                total_charge = room["price"] 
                # Assuming one night for simple calculations
                
                room["is_available"] = True
                room["guest"] = None
                print(f"\nSUCCESS: {guest_name} checked out from Room {room_num}.")
                print(f"Basic charge (one night assumption): ${total_charge:.2f}")
            else:
                print(f"\nERROR: Room {room_num} is already available (not booked).")
            break

    if not found:
        print(f"\nERROR: Room number {room_num} not found.")
def main_menu():
    """Displays the main menu and handles user input."""
    while True:
        print("\n*** Hotel Management Menu ***")
        print("1. Display All Rooms")
        print("2. Book a Room")
        print("3. Check Out a Room")
        print("4. Exit")
        choice = input("Enter your choice (1-4): ").strip()

        if choice == '1':
            display_rooms()
        elif choice == '2':
            book_room()
        elif choice == '3':
            checkout_room()
        elif choice == '4':
            print("Exiting program. Goodbye!")
            break
        else:
            print("Invalid choice. Please enter a number between 1 and 4.")

if __name__ == "__main__":
    main_menu()
