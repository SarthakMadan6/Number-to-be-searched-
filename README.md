# Number-to-be-searched-
#first the input is given to search a number
number=input("Enter a number :")
#the total count was set to 0
count=0
#x is defined by the length of the number
x = len(number)

#Now, if and else statement is written to check if the output is true or false 
if number.isdigit() == False:
    print("Number must be positive integer ! Try again \n")
else:
    number = int(number)
    digit = int(input("Enter number to be searched : "))
    if digit >= 10:
        print("Digit must be in range 0...9 ")
    else:
        y = number
#the for loop was included so to loop the program
        for i in range(0, x):
            x = 0
            x = int(y % 10)
            if digit == x:
                count += 1
            y = int(y / 10)
#At the end the loop was print statement was given so to print the whole code for program to work 
        print("Number of " + str(digit) + "'s in " + str(number) + " is " + str(count))
