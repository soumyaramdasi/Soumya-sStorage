# Soumya-sStorage
#python personal expense tracker mini project

#each expense in one dictionary like this: expense1={"category":"blah","amount":"blah","description":"blah blah blah"}
#each of these expense would be added to one list to store all expenses together

while True:
    print("="*54)
    var="PERSONAL EXPENSE TRACKER"
    print(var.center(54," "))
    print("="*54)
    print("1. Add New Expense",/n)
    print("2. View All Expenses")
    print("3. Category Summary")
    print("4. Set/Check Budget")
    print("5. Search Expenses")
    print("6. Exit")
    print("="*54)
    choice= int(input("Enter Your Choice (1-6):"))
    if choice == 1:
        print("Add New Expense: ")
    elif choice==2:
        print("View Expense: ")
    elif choice==3:
        print("Category Summary: ")
    elif choice==4:
        print("Set/Check Budget: ")
    elif choice==5:
        print("Searching Expenses: ")
    elif choice==6:
        print("Thank You For Using Personal Expense Tracker! Happy Budgeting!")
        break
    else:
        print("Invalid option, Please try again by inputting a number from 1-6.")
