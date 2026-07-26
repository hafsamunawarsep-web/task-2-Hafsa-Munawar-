# task-2-Hafsa-Munawar-
repository task 02
[decode task 02.py](https://github.com/user-attachments/files/30390826/decode.task.02.py)
# Expense Tracker Project

expenses = []
total = 0

while True:
    print("\n===== EXPENSE TRACKER =====")
    print("1. Add Expense")
    print("2. View Expenses")
    print("3. Show Total Spent")
    print("4. Exit")

    choice = input("Enter your choice (1-4): ")

    if choice == "1":
        amount = float(input("Enter expense amount: "))
        expenses.append(amount)
        total = total + amount
        print("Expense added successfully!")

    elif choice == "2":
        if len(expenses) == 0:
            print("No expenses added yet.")
        else:
            print("\nExpenses:")
            for i, expense in enumerate(expenses, start=1):
                print(f"{i}. Rs. {expense}")

    elif choice == "3":
        print(f"\nTotal Spent: Rs. {total}")

    elif choice == "4":
        print("Thank you for using Expense Tracker!")
        break

    else:
        print("Invalid choice! Please enter a number between 1 and 4.")
