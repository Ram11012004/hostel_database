# Simple Hostel Management System

# Initialize empty dictionaries to store details
students = {}
hostels = {}
wardens = {}
rooms = {}

def add_student():
    student_id = input("Enter Student ID: ")
    name = input("Enter Student Name: ")
    room_no = input("Enter Room Number: ")
    hostel_id = input("Enter Hostel ID: ")

    students[student_id] = {
        "Name": name,
        "Room No": room_no,
        "Hostel ID": hostel_id
    }
    print("Student added successfully!")

def add_hostel():
    hostel_id = input("Enter Hostel ID: ")
    name = input("Enter Hostel Name: ")
    location = input("Enter Hostel Location: ")

    hostels[hostel_id] = {
        "Name": name,
        "Location": location
    }
    print("Hostel added successfully!")

def add_warden():
    warden_id = input("Enter Warden ID: ")
    name = input("Enter Warden Name: ")
    hostel_id = input("Enter Hostel ID: ")

    wardens[warden_id] = {
        "Name": name,
        "Hostel ID": hostel_id
    }
    print("Warden added successfully!")

def add_room():
    room_no = input("Enter Room Number: ")
    hostel_id = input("Enter Hostel ID: ")
    capacity = input("Enter Room Capacity: ")

    rooms[room_no] = {
        "Hostel ID": hostel_id,
        "Capacity": capacity
    }
    print("Room added successfully!")

def view_students():
    for student_id, details in students.items():
        print(f"Student ID: {student_id}")
        print(f"Name: {details['Name']}")
        print(f"Room No: {details['Room No']}")
        print(f"Hostel ID: {details['Hostel ID']}")
        print("-" * 20)

def view_hostels():
    for hostel_id, details in hostels.items():
        print(f"Hostel ID: {hostel_id}")
        print(f"Name: {details['Name']}")
        print(f"Location: {details['Location']}")
        print("-" * 20)

def view_wardens():
    for warden_id, details in wardens.items():
        print(f"Warden ID: {warden_id}")
        print(f"Name: {details['Name']}")
        print(f"Hostel ID: {details['Hostel ID']}")
        print("-" * 20)

def view_rooms():
    for room_no, details in rooms.items():
        print(f"Room No: {room_no}")
        print(f"Hostel ID: {details['Hostel ID']}")
        print(f"Capacity: {details['Capacity']}")
        print("-" * 20)

def main_menu():
    while True:
        print("\nHostel Management System")
        print("1. Add Student")
        print("2. Add Hostel")
        print("3. Add Warden")
        print("4. Add Room")
        print("5. View Students")
        print("6. View Hostels")
        print("7. View Wardens")
        print("8. View Rooms")
        print("9. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            add_student()
        elif choice == "2":
            add_hostel()
        elif choice == "3":
            add_warden()
        elif choice == "4":
            add_room()
        elif choice == "5":
            view_students()
        elif choice == "6":
            view_hostels()
        elif choice == "7":
            view_wardens()
        elif choice == "8":
            view_rooms()
        elif choice == "9":
            print("Exiting the system. Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")

# Run the program
main_menu()
