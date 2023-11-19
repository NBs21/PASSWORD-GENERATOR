#-------------------------------------------------------------------------------
# Name:        PASSWORD GENERATOR
# Purpose:     Cod Soft TASK-3
# A password generator is a useful tool that generates strong and random passwords for users. This project aims to create a password generator application using Python, allowing users to specify the length and complexity of the password. User Input: Prompt the user to specify the desired length of the password. Generate Password: Use a combination of random characters to generate a password of the specified length.
Display the Password: Print the generated password on the screen.
# Author:      NURFUL SHAIKH
# Created:     07-11-2023
#-------------------------------------------------------------------------------
import string
import random
length = int(input("Enter password length: "))
print('''Choose character set for password from these :
         1. Digits
         2. Letters
         3. Special characters
         4. Exit''')
characterList = ""
while(True):
    choice = int(input("Pick a number "))
    if(choice == 1):
        characterList += string.digits
    elif(choice == 2):
        characterList += string.ascii_letters
    elif(choice == 3):
        characterList += string.punctuation
    elif(choice == 4):
        break
    else:
        print("Please pick a valid option!")
password = []
for i in range(length):
    randomchar = random.choice(characterList)
    password.append(randomchar)
print("The random password is " + "".join(password))
