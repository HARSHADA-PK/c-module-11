# c-module-11
# EXP NO:21
C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
# Aim: 
To write a C program to create a function to find the greatest number

# Algorithm:

1.Include the necessary header #include <stdio.h>.

2.Use a series of if and else if statements to compare the values and return the maximum among them.

3.Declare variables a, b, c, d, and greater to store user input and the result.

4.Use scanf to take four integers as input.

5.Call the max_of_four function with the input integers and store the result in the greater variable

# Program: 
```
#include<stdio.h>
int max(int x,int y)
{
    return (x>y)?x:y;
}
int max_of_four(int a,int b,int c,int d)
{
    return max(max(a,b),max(c,d));
}
int main()
{
    int a,b,c,d;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    printf("%d",max_of_four(a,b,c,d));
}
```

# Output: 
![image](https://github.com/user-attachments/assets/54498712-d5b2-414d-aeeb-69fd43f63820)


Result: Thus, the program that create a function to find the greatest number is verified successfully.

# EXP NO:22 
C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND XOR COMPARISONS 
# Aim: 
To write a C program to print the maximum values for the AND, OR and XOR comparisons

# Algorithm:

1.Define a function calculate_the_max that takes two integers n and k as parameters.

2.Declare variables a, b, and c to store the maximum values for AND, OR, and XOR operations, respectively.

3.Use nested loops to iterate through pairs of integers (i, j) from 1 to n.

4.Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, b, c).

5.Declare variables n and k to store user input.

6.Use scanf to take two integers as input.

7.Call the calculate_the_max function with input values.

# Program: 
```
#include<stdio.h>
void calculate_the_maximum(int n,int k)
{
    int max_and=0,max_or=0,max_xor=0;
    for(int a=1;a<n;a++)
    {
        for(int b=a+1;b<=n;b++)
        {
            int and_value=a & b;
            int or_value= a|b;
            int xor_value = a^b;
            if(and_value<k && and_value > max_and)
            {
                max_and=and_value;
            }
            if(or_value <k && or_value > max_or)
            {
                max_or=or_value;
            }
            if(xor_value < k && xor_value > max_xor)
            {
                max_xor=xor_value;
            }
        }
    }
    printf("%d\n",max_and);
    printf("%d\n",max_or);
    printf("%d\n",max_xor);
}
int main()
{
    int n,k;
    scanf("%d%d",&n,&k);
    calculate_the_maximum(n,k);
    return 0;
}
```

# Output: 
![image](https://github.com/user-attachments/assets/909d3e2c-a7ce-40b5-b82e-f400346773b0)


Result: Thus, the program to print the maximum values for the AND, OR and XOR comparisons is verified successfully.

# EXP NO:23 
C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS 
# Aim:
To write a C program to write the logic for the requests

# Algorithm:

1.Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.

2.Use scanf to take two integers as input for the number of shelves and queries.

3.Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.

4.Declare variables k and c to keep track of the book index and the total number of books.

5.Use a for loop to iterate over the queries.
# Program: 
```
#include <stdio.h>

#define MAX_SHELVES 100
#define MAX_BOOKS 100

int shelves[MAX_SHELVES][MAX_BOOKS];
int book_counts[MAX_SHELVES] = {0};

int main() {
    int num_shelves, num_queries;
    scanf("%d %d", &num_shelves, &num_queries);
    
    for (int i = 0; i < num_queries; i++) {
        int query_type;
        scanf("%d", &query_type);
        
        if (query_type == 1) {
            int x, y;
            scanf("%d %d", &x, &y);
            shelves[x][book_counts[x]++] = y;
        } else if (query_type == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", shelves[x][y]);
        } else if (query_type == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", book_counts[x]);
        }
    }
    
    return 0;
}
```
# Output: 
![image](https://github.com/user-attachments/assets/06022943-6aae-4e2b-9016-a6bf84117bd2)


Result: Thus, the program to write the logic for the requests is verified successfully.

# EXP NO:24
C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
# Aim: 
To write a C program print the sum of the integers in the array.

# Algorithm:

1.Declare a variable n to store the number of integers.

2.Use scanf to take an integer n as input.

3.Declare an array a of size n to store the integers.

4.Declare a variable sum and initialize it to zero.

5.Use a for loop to iterate n times:

6.Use scanf to input each integer and add it to the sum.

7.Print the final sum using printf.
# Program: 
```
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int n,sum=0;
    scanf("%d",&n);
    int *arr=(int*)malloc(n*sizeof(int));
    if(arr==NULL)
    {
        printf("Memory allocated");
        return 1;
    }
    for(int i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
        sum+=arr[i];
    }
    printf("%d",sum);
    free(arr);
    
}
```

# Output: 
![image](https://github.com/user-attachments/assets/1e31c5be-e6df-4abf-a2e3-162eee8336af)


Result: Thus, the program prints the sum of the integers in the array is verified successfully.

# EXP NO 25: 
C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE

# Aim:

To write a C program that counts the number of words in a given sentence.

# Algorithm:

1.Input the sentence: Take a sentence from the user.

2.Initialize a counter variable: This will keep track of the number of words.

3.Process each character of the sentence: o Iterate through the sentence, checking each character. o If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.

4.Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.

5.Display the result: After processing the sentence, output the total word count.
# Program: 
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    fgets(str,sizeof(str),stdin);
    int len=sizeof(str);
    int count=1;
     for(int i=0;i<len-1;i++){
         if(str[i]==' ')
         count++;
         
     }
     printf("Total number of words in the string is :%d",count);
    return 0;
}
```
# Output: 
![image](https://github.com/user-attachments/assets/5fb6f590-8866-4776-bdfb-c9eaa2c8be68)

Result:

Thus, the program that counts the number of words in a given sentence is verified successfully.
