# CMS-using-LIST

cust_id = []
cust_name = []
cust_age = []
cust_salary = []

def add_cust(id,name,age,salary):
    cust_id.append(id)
    cust_name.append(name)
    cust_age.append(age)
    cust_salary.append(salary)

def search_cust(id):
    index = cust_id.index(id)
    return index

def delete_cust(id):
    index = cust_id.index(id)
    cust_id.pop(index)
    cust_name.pop(index)
    cust_age.pop(index)
    cust_salary.pop(index)

def modify_cust(id,name,age,salary):
    index = cust_id.index(id)
    cust_name[index] = name
    cust_age[index] = age
    cust_salary[index] = salary








while True:
    print('Welcome to my Customer Management System')
    print('1. ADD Customer: \n 2. Search Customer: \n 3. Delete Customer: \n '
      '4. Modify Customer: \n 5. Display All Customer: ')

    choice = input('Enter your choice: ')

    if choice == '1':
        print('you choose Add customer detail option:')
        id = int(input('Enter the customer id: '))
        name = input('Enter the customer name: ')
        age = int(input('Enter the customer age: '))
        salary = int(input('Enter the customer salary: '))
        add_cust(id,name,age,salary)
        print('Your details is added successfully')


    elif choice == '2':
        print('You choose Search option:')
        id = int(input('Enter the customer id which you want to search: '))
        index = search_cust(id)
        print('Cust_id:',id,'Cust_name:',cust_name[index],'Cust_age:',
              cust_age[index],'Cust_salary:',cust_salary[index])

    elif choice == '3':
        print('You choose Delete option:')
        id = int(input('Enter the customer id which you want to delete: '))
        delete_cust(id)
        print('Your details is deleted successfully')

    elif choice == '4':
        print('You choose Modify option: ')
        id = int(input('Enter the customer id which you want to modify: '))
        name = input('Enter the customer modify name: ')
        age = int(input('Enter the customer modify age: '))
        salary = int(input('Enter the customer modify salary: '))
        modify_cust(id,name,age,salary)
        print('Customer details modified successfully')


    elif choice == '5':
        for i in range(len(cust_id)):
            print('Cust_id:',cust_id[i],'Cust_name:',cust_name[i],
                  'Cust_age:',cust_age[i],'Cust_salary:',cust_salary[i])
