# login-using-python-tkinter


from tkinter import *

def login():
    username = username_entry.get()
    password = password_entry.get()
    
    # Add your authentication logic here
    # For simplicity, let's assume the username is "admin" and the password is "password"
    if username == "admin" and password == "password":
        login_status_label.config(text="Login successful!", fg="green")
    else:
        login_status_label.config(text="Login failed. Invalid username or password.", fg="red")

# Create the main window
window = Tk()
window.title("Login")

# Create username label and entry
username_label = Label(window, text="Username:")
username_label.pack()
username_entry = Entry(window)
username_entry.pack()

# Create password label and entry
password_label = Label(window, text="Password:")
password_label.pack()
password_entry = Entry(window, show="*")  # Show asterisks instead of the actual password
password_entry.pack()

# Create login button
login_button = Button(window, text="Login", command=login)
login_button.pack()

# Create label for displaying login status
login_status_label = Label(window, text="")
login_status_label.pack()

# Start the main event loop
window.mainloop()
