# Project01-Admission-Portal
import time
print(" ********Welcome to the Online Admission Portal ******** ")
time.sleep(1)

name = input(" Enter your name: \n").upper()
print("Hi,", name, ".", "It is an Online Portal for Universities' Admissions ")
time.sleep(2)
score = int(input("Enter your Fsc's Score:"))

time.sleep(2)
print("Enter the university name on which you want to apply. Here are the options: ")

uni = ["GIKI", "NUST", "UET", "NED"]                            #universities' names.
print(uni, ":")
def quiz():
    print("Well, The Questions are very easy.\n")
    time.sleep(2)
    print("Be alert while answering the questions")
    time.sleep(2)
    i = 0
    q1 = input("1.Spaghetti is the singular word of the word spaghetti.(true/false").upper()
    if q1 == "TRUE":
        i += 1
    time.sleep(3)
    q2 = input("2.The Capital of Australia is Sydney.(true/false)").upper()
    if q2 == "FALSE":
        i += 1
    q3 = input("3.The Moon is wider than Australia(true/false)").upper()
    if q3 == "FALSE":
        i += 1
    print("Here is your last Question:\n")
    print("What do you think?")
    time.sleep(3)
    q4 = int(input("How many questions you have entered correct(1,2,3). Answer this question carefully you can gain 2 points for answering correctly:"))
    if q4 == int(i):
        i = i + 2
        return i
def details():
    print("Select the program:")
    print("\n", "1.BS in Mechanical Engineering", "\n", "2.BS in Electrical Engineering",
          "\n", "3.BS in Chemical Engineering", "\n", "4.BS in Computer Engineering")

    degree = input("Enter the degree: ").upper()
    phoneNumber = int(input("Enter your Phone number! "))
    age = int(input("Enter your age:"))
    print("We are sending you the details of your personal information.", "\n")
    print("Please wait! It will take a while", "\n")
    time.sleep(4)
    print("Your name:", name)
    print("Your age:", age)
    print("Your cellphone number: ", phoneNumber)
    print("University name is: ", uniName)
    print("Applying in", degree, "\n\n\n")
    time.sleep(3)
    print("Thank you for using Ahmed's Online Admission Helper for Free!")

uniName = input().upper()
if uniName == "GIKI" or "NUST" or "NED" or "UET":
    if score > 800:
        details()

    else:
        print("You cannot apply in", uniName, "university")
        time.sleep(2)
        print("Wait!")
        time.sleep(2)
        print("But!!Do not worry!!.\nWe can do something for you!\n")
        time.sleep(2)
        print("If you answer 3 out of 4 questions correctly, then you can gain extra 250 numbers in your score,",uniName,"university")
        time.sleep(3)
        ans = input("Do you want to answer (yes/no)").upper()
        if ans == "YES":
            i=quiz()
            if i >= 3:
                print("You have entered", i, "correct answers")
                score = 250+score
                details()
            else:
                print("You can now leave!","U0001F606")

