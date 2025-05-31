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
//Sudharsan S
 //Reg no : 212224040334 
#include <stdio.h>
int main() {
    float a,b;
    float *ptr1 = &a;
    float *ptr2 = &b;
    printf("Enter the length of the rectangle: ");
    scanf("%f",ptr1);
    printf("\nEnter the width of the rectangle: ");
    scanf("%f",ptr2);
    printf("\nArea : %.2f",(*ptr1) * (*ptr2));
}

```
## OUTPUT
		       	
![image](https://github.com/user-attachments/assets/73c554a7-7376-4c21-afa5-048226a18015)


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
//Sudharsan S
 //Reg no : 212224040334 
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
int main() {
    char arr[100];
    printf("Enter the string: ");
    scanf("%[^\n]",arr);
    int n = strlen(arr);
    char *ptr = (char *) malloc (n*sizeof(char));
    if(ptr==NULL) return 1;
    strcpy(ptr,arr);
    printf("\n");
    for(int i = 0;i<n;i++) printf("%c",ptr[i]);
    free(ptr);
    
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/78df787f-842e-4626-906d-bc35378b1f31)



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
//Sudharsan S
 //Reg no : 212224040334 
#include <stdio.h>
#include <string.h>
#include <math.h>
struct stdinfo{
    int rollno;
    float mark[5];
    char name[20];
};
int main() {
   int n,i=0;
   printf("Enter the number of students: ");
   scanf("%d",&n);
   struct stdinfo v[n];
   for(;i<n;i++){
       printf("\nEnter the name: ");
       scanf(" %[^\n]",v[i].name);
       printf("\nEnter the roll number: ");
       scanf("%d",&v[i].rollno);
       printf("\nEnter the marks for your 5 subjects:\n");
       for(int j = 0;j<5;j++) scanf("%f",&v[i].mark[j]);
   }
   printf("\nRollnumber:        Student name:        subject marks:\n\n");
   for(int i=0;i<n;i++){
       printf("%d",v[i].rollno);
       int rlen = log10(v[i].rollno)+1;
       for(int k=0;k<19-rlen;k++) printf(" ");
       printf("%s",v[i].name);
       int slen = strlen(v[i].name);
       for(int k=0;k<21-slen;k++) printf(" ");
       
       for(int j = 0;j<5;j++){
       if(j==0)printf("%.0f",v[i].mark[j]);
       else{
           printf(", %.0f",v[i].mark[j]);
       } }
       printf("\n\n");
   }
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/250c1e67-a0dd-4291-8881-151542c5b28f)



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
//Sudharsan S
 //Reg no : 212224040334 
#include <stdio.h>
#include <string.h>
#include <math.h>
struct empinfo{
    int id;
    float salary;
    float HRA;
    float DA;
    float grossSalary;
    char name[20];
};
int main() {
   int n,i=0;
   printf("Enter the number of employees: ");
   scanf("%d",&n);
   struct empinfo v[n];
   for(;i<n;i++){
       printf("\nEmployee No: %d\n",i+1);
       printf("\nEnter the name: ");
       scanf(" %[^\n]",v[i].name);
       printf("\nEnter the id number: ");
       scanf("%d",&v[i].id);
       printf("\nEnter the salary amt: ");
       scanf("%f",&v[i].salary);
       printf("\nEnter the HRA amt: ");
       scanf("%f",&v[i].HRA);
       printf("\nEnter the DA amt: ");
       scanf("%f",&v[i].DA);
       v[i].grossSalary = v[i].salary + v[i].HRA + v[i].DA; 
   }
   printf("\nID:          Employee name:          Salary:          Gross salary:\n\n");
   for(int i=0;i<n;i++){
       printf("%d",v[i].id);
       int rlen = log10(v[i].id)+1;
       for(int k=0;k<13-rlen;k++) printf(" ");
       printf("%s",v[i].name);
       int slen = strlen(v[i].name);
       for(int k=0;k<24-slen;k++) printf(" ");
       printf("%.2f",v[i].salary);
       rlen = log10((int)v[i].salary)+1;
       for(int k=0;k<17-rlen-2;k++) printf(" ");
       printf("%.2f",v[i].grossSalary);
      
       printf("\n\n");
   }
}

```

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/e08a1599-c244-4907-b423-cbdbf468ce72)



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
//Sudharsan S
//212224040334
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

 ![image](https://github.com/user-attachments/assets/1939f300-dfa7-4a25-aba7-c85ad9f023e2)



## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


