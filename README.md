import datetime

appointments = {}  # Dictionary to store appointments

def book_appointment(patient_name, doctor_name, date, time):
    """Books an appointment."""
    appointment_id = len(appointments) + 1
    appointments[appointment_id] = {
        "patient_name": patient_name,
        "doctor_name": doctor_name,
        "date": date,
        "time": time,
    }
    print(f"Appointment booked successfully. Your appointment ID is: {appointment_id}")

def view_appointment(appointment_id):
    """Views an appointment."""
    if appointment_id in appointments:
        appointment = appointments[appointment_id]
        print(f"Patient Name: {appointment['patient_name']}")
        print(f"Doctor Name: {appointment['doctor_name']}")
        print(f"Date: {appointment['date']}")
        print(f"Time: {appointment['time']}")
    else:
        print("Appointment not found.")


# Example usage
book_appointment("Alice", "Dr. Smith", datetime.date(2024, 3, 15), "10:00")
view_appointment(1)
