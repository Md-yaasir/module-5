## REG-NO: 212224040196
## DATE : 27-04-25
## EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

int main() {
    int length, breadth, area;
    int *p1 = &length, *p2 = &breadth;

    printf("Enter length of rectangle: ");
    scanf("%d", p1);

    printf("Enter breadth of rectangle: ");
    scanf("%d", p2);

    area = (*p1) * (*p2);

    printf("Area of rectangle: %d\n", area);

    return 0;
}

```

## OUTPUT
![Screenshot 2025-04-27 133532](https://github.com/user-attachments/assets/3e65a19e-9e4e-4dc4-b068-087c4dc26943)

		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    char *str;
    str = (char *)malloc(8 * sizeof(char));

    if (str == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }

    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0';

    printf("%s\n", str);

    free(str);

    return 0;
}

```

## OUTPUT
![Screenshot 2025-04-27 133651](https://github.com/user-attachments/assets/e29869be-0da7-4786-beb5-03ad0c86e240)



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 

# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

struct Student {
    int roll_no;
    char name[50];
    float marks;
};

int main() {
    struct Student s;

    printf("Enter roll number: ");
    scanf("%d", &s.roll_no);

    printf("Enter name: ");
    scanf("%s", s.name);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    printf("\nStudent Information:\n");
    printf("Roll Number: %d\n", s.roll_no);
    printf("Name: %s\n", s.name);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}
```


## OUTPUT
![Screenshot 2025-04-27 133849](https://github.com/user-attachments/assets/14f03db5-0599-46b6-b190-0c5cbe59f709)



## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

struct Employee {
    char name[100];
    int id;
    float basic_salary;
    float gross_salary;
};

int main() {
    struct Employee emp[3];

    for (int i = 0; i < 3; i++) {
        printf("Enter details of employee %d\n", i + 1);

        printf("Enter name: ");
        scanf(" %[^\n]", emp[i].name);

        printf("Enter ID: ");
        scanf("%d", &emp[i].id);

        printf("Enter basic salary: ");
        scanf("%f", &emp[i].basic_salary);

        emp[i].gross_salary = emp[i].basic_salary + (0.8 * emp[i].basic_salary) + (0.2 * emp[i].basic_salary);
    }

    printf("\nEmployee Details:\n");
    for (int i = 0; i < 3; i++) {
        printf("\nEmployee %d\n", i + 1);
        printf("Name: %s\n", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("Gross Salary: %.2f\n", emp[i].gross_salary);
    }

    return 0;
}

```


 ## OUTPUT
 ![Screenshot 2025-04-27 134211](https://github.com/user-attachments/assets/b5cbc24a-0387-4008-951b-ae9b7b7ac8a1)


 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```c
#include <stdio.h>

struct Student {
    char name[50];
    int roll_no;
    float marks[5];
    float total;
    float average;
};

int main() {
    struct Student s;

    printf("Enter student details:\n");
    
    printf("Enter name: ");
    scanf("%s", s.name);
    
    printf("Enter roll number: ");
    scanf("%d", &s.roll_no);

    s.total = 0;

    for (int i = 0; i < 5; i++) {
        printf("Enter marks for subject %d: ", i + 1);
        scanf("%f", &s.marks[i]);
        s.total += s.marks[i];
    }

    s.average = s.total / 5;

    printf("\nStudent Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.roll_no);
    
    printf("Marks: ");
    for (int i = 0; i < 5; i++) {
        printf("%.2f ", s.marks[i]);
    }
    printf("\n");

    printf("Total Marks: %.2f\n", s.total);
    printf("Average Marks: %.2f\n", s.average);

    return 0;
}

```


## OUTPUT
![Screenshot 2025-04-27 134434](https://github.com/user-attachments/assets/d8a1afc9-a6cc-4b65-b67e-84088d7b9568)

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


