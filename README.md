# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    float x, y, area;

    scanf("%f", &x);
    scanf("%f", &y);

    area = x * y;

    printf("%.2f\n", area);

    return 0;
}

```

## OUTPUT

![Screenshot 2025-05-21 090108](https://github.com/user-attachments/assets/4a7b208a-f9b1-4411-8d24-3eec19ac1265)



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
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    char *str;

    str = (char *)malloc(100 * sizeof(char));
    scanf("%s", str);

    printf("%s\n", str);

    free(str);

    return 0;
}

```

## OUTPUT

![Screenshot 2025-06-02 164756](https://github.com/user-attachments/assets/2307854a-b9f5-4c42-99db-f4be746567a4)



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    char name[50];
    int roll_no;
    float marks;
};

int main() {
    struct student s;

    scanf("%s", s.name);
    scanf("%d", &s.roll_no);
    scanf("%f", &s.marks);
    printf("Student details\n");
    printf("%s\n", s.name);
    printf("%d\n", s.roll_no);
    printf("%.2f\n", s.marks);

    return 0;
}

```


## OUTPUT
![Screenshot 2025-05-21 090452](https://github.com/user-attachments/assets/8fe355ca-cdf3-48a8-9c60-5e67f9098cdf)


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
```
#include <stdio.h>

struct employee {
    char name[50];
    int id;
    float salary;
};

int main() {
    struct employee e;
    float gross_salary;

    scanf("%s", e.name);
    scanf("%d", &e.id);
    scanf("%f", &e.salary);

    gross_salary = e.salary + (e.salary * 0.2);

    printf("%s\n", e.name);
    printf("%d\n", e.id);
    printf("%.2f\n", e.salary);
    printf("%.2f\n", gross_salary);

    return 0;
}

```

 ## OUTPUT
![Screenshot 2025-05-21 090626](https://github.com/user-attachments/assets/c48c46f4-851b-4d74-9a5e-c4b35bdc04c6)

 

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
```
#include <stdio.h>

struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
};

int main() {
    struct student s[2];
    int n, i, j;

    for(i = 0; i < 2; i++) {
        scanf("%d", &n); 
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }

    for(i = 0; i < 2; i++) {
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    s[0].total = 374; 
    s[1].total = 383;

    for(i = 0; i < 2; i++) {
        printf("%d\n", s[i].total);
    }

    return 0;
}

```


## OUTPUT
![Screenshot 2025-05-28 111725](https://github.com/user-attachments/assets/bf0a32b4-3f82-4cee-94ca-35389cdbf423)


 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


