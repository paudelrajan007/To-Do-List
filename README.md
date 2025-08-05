
README.md
markdown
Copy
Edit

# Simple To-Do List Manager (Python)

## Objective

This project is a basic to-do list manager built using Python. It lets users add, update, delete, and view tasks through a command-line interface.

## Features

- Add tasks
- Update tasks
- Delete tasks
- View all tasks
- Exit the program

## How to Run

1. Save the code in a file, for example: `todo_list.py`
2. Open a terminal and run:

python todo_list.py

markdown
Copy
Edit

## How It Works

- The program first asks how many tasks you want to add.
- After entering the initial tasks, a menu appears.
- You can choose from the menu:
  - Add a new task
  - Update an existing task
  - Delete a task
  - View all tasks
  - Exit the program

## Requirements

- Python 3.x
- No external libraries

## Note

- Tasks are stored only during the session (not saved to a file).

## My Code

# Objective: Implement a simple to-do list manager.

def task():
tasks = [] # empty list
print("Welcom to TO-DO-LIST MANAGER ..")
total_task = int(input("Enter total number of today task..")) # how many task you want (1 to your wish)

    for i in range(1, total_task + 1):
        task_name_list = input(f"Enter task {i}= ")  # enter task
        tasks.append(task_name_list)  # adds a new item to the end of a list

    print(f"Today's tasks are\n{tasks} ")

    while True:
        option = int(input("Enter 1-Add the task \n 2- Update the task 3- Delete the task 4- View all tasks \n 5- Exixt or Stop "))

        if option == 1:
            add = input("Enter task you want to add = ")
            tasks.append(add)
            print(f"Task {add} has been successfully added.")

        elif option == 2:
            update_value = input("Enter the task you want to update = ")
            new_task = input("Enter new Task = ")
            if update_value in tasks:
                index = tasks.index(update_value)
                tasks[index] = new_task
                print(f"Updated task {new_task}")
            else:
                print("Task not found.")

        elif option == 3:
            deleted_value = input("Enter Which task you want to delete = ")
            if deleted_value in tasks:
                index = tasks.index(deleted_value)
                del tasks[index]
                print(f"Task {deleted_value} has been deleted ")
            else:
                print("Task not found.")

        elif option == 4:
            print(f"Total tasks={tasks}")

        elif option == 5:
            print("Exit the program ")
            break

        else:
            print("There is no Option :- Invalid")

task()
=======
# Objective: Implement a simple to-do list manager.
def task():
    tasks = []  # empty list
    print("Welcom to TO-DO-LIST MANAGER ..")
    total_task = int(input("Enter total number of today task.."))  # how many task you want (1 to your wish)

    for i in range(1, total_task + 1):
        task_name_list = input(f"Enter task {i}= ")  # enter task 
        tasks.append(task_name_list)  # adds a new item to the end of a list 

    print(f"Today's tasks are\n{tasks} ")

    while True:
        option = int(input("Enter 1-Add the task \n 2- Update the task 3- Delete the task 4- View all tasks \n 5- Exixt or Stop "))
        
        if option == 1:
            add = input("Enter task you want to add = ")
            tasks.append(add) 
            print(f"Task {add} has been successfully added.")

        elif option == 2:
            update_value = input("Enter the task you want to update = ")
            new_task = input("Enter new Task = ")
            if update_value in tasks:
                index = tasks.index(update_value) 
                tasks[index] = new_task
                print(f"Updated task {new_task}")
            else:
                print("Task not found.")

        elif option == 3:
            deleted_value = input("Enter Which task you want to delete = ")
            if deleted_value in tasks: 
                index = tasks.index(deleted_value)
                del tasks[index]
                print(f"Task {deleted_value} has been deleted ")
            else:
                print("Task not found.")

        elif option == 4:
            print(f"Total tasks={tasks}") 

        elif option == 5:
            print("Exit the program ")
            break

        else:
            print("There is no Option :- Invalid")

task()
>>>>>>> 2a9aa0efed98fad5e2e79e9494c3e740b7e444f5
