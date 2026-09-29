# Student-Manager-App
student ={}

while True:
    print("\n-----Student Manager App-----")
    print("1.Add student")
    print("2.View student")
    print("3.Check result")
    print("4.Exist")

    choice = input("Enter Your Choice:")

    #add student
    if choice == "1":
        name = input("Enter student name:")
        marks = int(input("Enter marks:"))
        student[name] = marks
        print(f"{name} Successfully Added!")


    #view student 
    elif choice == "2":
        if not student:
            print("No student found!")
        else:
            for name,marks in student.items():
                print(name,":",marks)

    #check result
    elif choice == "3":
        name = input("Enter student name:")

        if name in student:
            marks = student[name]

            if marks >= 40:
                print("Pass")
            else:
                print("Fail")

        else:
            print("Student not found!")


    #exist
    elif choice == "4":
        print("Existing")
        break

    else:
        print("In valid input")