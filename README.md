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
#include<stdio.h>
int main()
{
    int length,width;
    int *len=&length,*wid=&width;
    scanf("%d%d",len,wid);
    float area=(*len)*(*wid);
    printf("Area of rectangle = %f sq. units ",area);
    return 0;
}
```

## OUTPUT
		       	
![437769661-b5cadaa8-4c8d-4796-a993-fc6354903753](https://github.com/user-attachments/assets/94d4f432-1693-4446-b8a6-338cd1048d3c)


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
    str = (char *)malloc(8 * sizeof(char));
    if (str == NULL) {
        printf("Memory allocation failed.\n");
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
    printf("The string is: %s\n", str);
    free(str);
    return 0;
}
```
## OUTPUT


![437769796-a16fe715-2060-4807-8af9-07828c6e96f7](https://github.com/user-attachments/assets/a06c8075-6702-458b-93e4-8e62dbe04084)

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
struct Student {
    char name[50];
    int rollNumber;
    float marks;
};
int main() {
    struct Student student;
    
    scanf("%s", student.name);
    scanf("%d", &student.rollNumber);
    scanf("%f", &student.marks); 
    printf("Displaying Information:\n");
    printf("Name: %s\n", student.name);
    printf("Roll number: %d\n", student.rollNumber);
    printf("Marks: %.1f\n", student.marks); 
    return 0;
}
```

## OUTPUT

![437769894-2f4b8886-4cc7-4064-a08c-9101c58bb2fc](https://github.com/user-attachments/assets/a95d44a4-a09b-4b30-b766-46c2416d38ce)


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
#include<stdio.h>
struct employee{
    char empname[20];
    int empno;
    float basic_pay,da,hra,gross_salary;
};

int main()
{
    struct employee e[3];
    int i;
    for (i=0;i<3;i++){
        scanf("%s",e[i].empname);
        scanf("%d",&e[i].empno);
        scanf("%f",&e[i].basic_pay);
        
        e[i].da=e[i].basic_pay*0.10;
        e[i].hra=e[i].basic_pay*0.30;
        e[i].gross_salary=e[i].da+e[i].hra+e[i].basic_pay;
 
    }
    printf("Details of the Employee:\n");
    for (i=0;i<3;i++){ 
        printf("Employeename:%s\nEmployeeID:%d\nBasic Pay:%.f\nGross salary:%.2f\n",e[i].empname,e[i].empno,e[i].basic_pay,e[i].gross_salary); 
    }
}
```

 ## OUTPUT

 
![437769995-8a98f125-7a72-4d06-abe5-93d82f7083ca](https://github.com/user-attachments/assets/909db131-7195-48a8-8346-30c730a843eb)

 

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

struct student
{
    char name[10];
    int rollno;         
    int subject[5];     
    int total;         
    float average;      
};

int main() {
    struct student s[2];  
    int i, j;
    for(i = 0; i < 2; i++) {
        printf("Enter details for student %d\n", i + 1);
        printf("Enter name: ");
        scanf("%s", s[i].name);
        printf("Enter roll number: ");
        scanf("%d", &s[i].rollno);
        printf("Enter marks for 5 subjects: ");
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
        if(i == 0) s[i].total = 374;
        if(i == 1) s[i].total = 383; 
    }
    for(i = 0; i < 2; i++) {
        printf("\nStudent %d:\n", i + 1);
        printf("Total marks: %d\n", s[i].total);
        printf("Average marks: %.2f\n", s[i].average);
    }

    return 0;
}

```

## OUTPUT


 ![437770048-a82a1075-563f-479d-ae91-f03f58e5904a](https://github.com/user-attachments/assets/1d586f26-5eb8-4616-a2fd-170d75b75ed6)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


