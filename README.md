def add_expense(date, amount, category, description):

    with open('daily_expenses.txt', 'a') as file:
        file.write(f'{date},{amount},{category},{description}\n')
    print('Expense added successfully!')
 
 
def view_expenses():
    try:
        with open('daily_expenses.txt', 'r') as file:
            print("Date "
            "| Amount "
            "| Category "
            "| Description")
            print("-" )
            for line in file:
                date, amount, category, description = line.strip().split(',')
                print(f"{date} |  ₹{amount} |   {category} | {description}")
    except FileNotFoundError:
        print("You haven't added any expenses yet.")
    


def main():

    while True:
        print("\nDaily Expense Tracker")
        print("1. Add Expense")
        print("2. View Expenses")
       
        print("3. Exit")
        
        choice = input("Pick any option: ")
        if choice == '1':
            date = input(" Date (DD-MM-YYYY): ")
            amount = input(" amount: ")
            category = input("category (e.g., Food, Transport): ").capitalize()
            description = input(" Describe it: ")
            add_expense(date, amount, category, description)
        elif choice == '2':
            view_expenses()
      
        elif choice == '3':
            print("All done .See  you next time!")
            break
        else:
            print("That option dosen't work.try again")

if __name__ == "__main__":
    main()

