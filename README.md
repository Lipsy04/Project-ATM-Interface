# Project-ATM-Interface
An ATM interface having details of balance, withdrawn and deposit amount
import time

print("Please insert your CARD")
time.sleep(5)

password= 1234
choice = 0
pin = int(input("Enter your atm pin: "))

balance= 50000

if pin == password:
    
    while choice != 4:
        print("""MENU
            1 == balance
            2 == withdraw balance
            3 == deposit balance
            4 == exit
               """
             )
        choice = int(input("\nEnter your option:\n"))
        
        if choice==1:
            print("Balance = Rs", balance)
            
        elif choice==2:
            wit = int(input("Enter your withdraw amount = Rs"))
            balance -= wit
            print("\nwithdrawn amount: Rs",wit)
            print("Balance = Rs",balance)
            
        elif choice==3:
            dep = int(input("Enter your deposit amount = Rs"))
            balance += dep
            print("\nDeposited amount: Rs",wit)
            print("Balance = Rs",balance)
            
        elif choice==4:
            print("\nSession Ended!! GOODBYE")  
    
else:
    print("Wrong Pin, Please TRY AGAIN! ")
