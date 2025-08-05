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
