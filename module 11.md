

**EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER**

**Aim:**
To write a C program to create a function to find the greatest number

**Algorithm:**
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
**Program:**
```
#include<stdio.h>
int max_of_four(int n1,int n2,int n3,int n4)
{
    int max=n1;
    if(n2>max)
    {
        max=n2;
    }
    if(n3>max)
    {
        max=n3;
    }
    if(n4>max)
    {
        max=n4;
    }
    return max;
}
int main()
{
    int n1,n2,n3,n4,r;
    scanf("%d%d%d%d",&n1,&n2,&n3,&n4);
    r=max_of_four(n1,n2,n3,n4);
    printf("%d",r);
}

```

**Output:**

<img width="354" height="311" alt="image" src="https://github.com/user-attachments/assets/0680351b-6d51-4062-8b14-a09bcd78b331" />


**Result:**

Thus, the program  that create a function to find the greatest number is verified successfully.


 
**EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS**

**Aim:**
To write a C program to print the maximum values for the AND, OR and XOR comparisons

**Algorithm:**
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
**Program:**

```
#include<stdio.h>
#include<math.h>
void calculate_max(int n,int k)
{
    int max_and=0,max_or=0,max_xor=0;
    for(int a=1;a<=n;a++){
        for(int b=a+1;b<=n;b++){
            int and_val=a&b;
            int or_val=a|b;
            int xor_val=a^b;
            if(and_val<k&&and_val>max_and)
              max_and=and_val;
            if(or_val<k&&or_val>max_or)
              max_or=or_val;
            if(xor_val<k&&xor_val>max_xor)
              max_xor=xor_val;
        }
    }
    printf("%d\n%d\n%d\n",max_and,max_or,max_xor);
}
int main()
{
    int n,k;
    scanf("%d%d",&n,&k);
    calculate_max(n,k);
    return 0;
}
    
```
**Output:**

<img width="290" height="412" alt="image" src="https://github.com/user-attachments/assets/b6b9262e-0a9e-47ca-93c6-9fe3076cc2f7" />


**Result:**

Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 

**EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS**

**Aim:**
To write a C program to write the logic for the requests

**Algorithm:**
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
**Program:**
```
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int n; // number of shelves
    scanf("%d", &n);
    int q; // number of queries
    scanf("%d", &q);
    // Create arrays to hold books and their counts
    int **total_number_of_pages = (int **)malloc(n * sizeof(int *)); // pages on each shelf
    int *total_number_of_books = (int *)malloc(n * sizeof(int));      // count of books per shelf
    // Initialize all shelves as empty
    for (int i = 0; i < n; i++)
    {
        total_number_of_books[i] = 0;
        total_number_of_pages[i] = NULL;
    }
    for (int i = 0; i < q; i++)
    {
        int type;
        scanf("%d", &type);
        if (type == 1) {
            // Query 1: Insert a book
            int x, y;
            scanf("%d %d", &x, &y);
            // Increase book count for that shelf
            total_number_of_books[x]++;
            // Reallocate memory for the new book
            total_number_of_pages[x] = realloc(total_number_of_pages[x],
                                               total_number_of_books[x] * sizeof(int));
            // Add the new book's page count at the end
            total_number_of_pages[x][total_number_of_books[x] - 1] = y;
        }
        else if (type == 2)
        {
            // Query 2: Print number of pages in y-th book on x-th shelf
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", total_number_of_pages[x][y]);
        }
        else if (type == 3)
        {
            // Query 3: Print number of books on x-th shelf
            int x;
            scanf("%d", &x);
            printf("%d\n", total_number_of_books[x]);
        }
    }
    // Free allocated memory
    for (int i = 0; i < n; i++)
    {
        free(total_number_of_pages[i]);
    }
    free(total_number_of_pages);
    free(total_number_of_books);

    return 0;
}

```


**Output:**

<img width="448" height="315" alt="image" src="https://github.com/user-attachments/assets/4459b5cd-8bb9-4d42-b19a-04c9bc3b39db" />


**Result:**

Thus, the program to write the logic for the requests is verified successfully.


 
**EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.**

**Aim:**
To write a C program print the sum of the integers in the array.

**Algorithm:**
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



**Program:**
```
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int n;
    int *arr;
    int sum=0;
    scanf("%d",&n);
    arr=(int*)malloc(n*sizeof(int));
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    for(int i=0;i<n;i++)
    {
        sum+=arr[i];
    }
    printf("%d\n",sum);
    free(arr);
    return 0;
}
```

**Output:**

 
<img width="433" height="215" alt="image" src="https://github.com/user-attachments/assets/d6a53aa1-b3d8-407f-9fda-c81997b5f4fd" />


**Result:**

Thus, the program prints the sum of the integers in the array is verified successfully.


 
**EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A  SENTENCE**



**Aim:**

To write a C program that counts the number of words in a given sentence.

**Algorithm:**

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



**Program:**
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int count=0;
    fgets(str,sizeof(str),stdin);
    for(int i=0;str[i];i++){
        if((str[i]==' '&&str[i+1]!=' '&&str[i+1]!='\0')||(i==0&&str[i]!=' ')){
            count++;
        }
    }
    printf("Total number of words in the string is :%d", count);
    return 0;
}
```

**Output:**

<img width="900" height="295" alt="image" src="https://github.com/user-attachments/assets/cb2a1cda-d98f-4313-a9b8-b309f99be643" />



**Result:**

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
