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
        print("Chosen Option: Add New Expense \n")
        print("ADD NEW EXPENSE".center(54,"-"))
        categories= ["Food","Transport","Entertainment","Shopping","Bills","Others"]
        print(f"Available Categories: {", ".join(categories[:])} ")
        category= input("Enter Category of Item: ").title()
        amount= float(input("Enter amount: "))
        description= input("Enter Description: ")
        #print(f"Category is {category}, Amount is {amount}, description is {description}")
        expense1={}
        expense1["Category"]=category
        expense1["Amount"]= amount
        expense1["Description"]=description
        expenses.append(expense1)
        print(" ")
        print("Expense Added Successfully! ✅")
        print(" ")
        print("Your Expenses are as below: ")
        sum=0
        for i in expenses:
            print(i["Category"], i["Amount"], i["Description"], "\n")
            sum= sum + i["Amount"]
    elif choice==2:
        print("View Expense: ")
        print("Chosen Option: View Expenses: \n")
        print("ALL EXPENSES".center(54,"-"))
        count=1
        total=0
        for i in expenses:
            print(f"#{count}   |   {i['Category']}   |   {i['Amount']}   |   {i['Description']}")
            count=count+1
            total=total+ i['Amount']
        print("-"*54)
        print(f"Total Expenses: ₹{total}")
        print(f"Total no. of expenses made: {count-1}\n")
    elif choice==3:
        print("Category Summary: ")
        print("Chosen Option: Category-Wise Summary: \n")
        print("CATEGORY-WISE SUMMARY".center(54,"-"))
        food_total= 0
        entertainment_total= 0
        transport_total= 0
        shopping_total= 0
        bills_total= 0
        others_total= 0
        for i in expenses:
            if i["Category"]== "Food":
                food_total= food_total +i["Amount"]
            elif i["Category"]== "Entertainment":
                entertainment_total=entertainment_total+i["Amount"]
            elif i["Category"]== "Transport":
                transport_total=transport_total+i["Amount"]
            elif i['Category']== "Shopping":
                shopping_total=shopping_total+i["Amount"]
            elif i['Category']== "Bills":
                bills_total=bills_total+i["Amount"]
            elif i['Category']== "Others":
                others_total=others_total+i["Amount"]
            print(i["Category"], i["Amount"])
        if food_total != 0:
            print(f"Total Amount Spent on Food: {food_total}")
        if entertainment_total != 0:
            print(f"Total Amount Spent on Entertainment: {entertainment_total}")
        if transport_total != 0:
            print(f"Total Amount Spent on Transport: {transport_total}")
        if shopping_total != 0:
            print(f"Total Amount Spent on Shopping: {shopping_total}")
        if bills_total != 0:
            print(f"Total Amount Spent on Bills: {bills_total}")
        if others_total != 0:
            print(f"Total Amount Spent on Others: {others_total}")
    elif choice==4:
        print("Set/Check Budget: ")
    elif choice==5:
        print("Searching Expenses: ")
    elif choice==6:
        print("Thank You For Using Personal Expense Tracker! Happy Budgeting!")
        break
    else:
        print("Invalid option, Please try again by inputting a number from 1-6.")
