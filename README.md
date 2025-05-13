# EX-16-BIT-WISE-OPERATION

## AIM

Write a C Program to perform bitwise AND operation of two integers. 

## ALGORITHM

```
1.Start
2.Declare three integer variables: num1, num2, result
3.Input the first integer and store it in num1
4.Input the second integer and store it in num2
5.Perform bitwise AND operation:
 result = num1 & num2
6.Output the result with a message:
 "Bitwise-AND result is = result"
7.End
```

## PROGRAM

```
#include <stdio.h>

int main() {
    int num1, num2, result;
    scanf("%d", &num1);
    scanf("%d", &num2);
    result = num1 & num2;
    printf("Bitwise-AND result is = %d\n", result);
    
    
    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/5faf4b94-46dc-49ec-8fa5-19894624139e)


## RESULT

Thus the Program to perform bitwise AND operation of two integers has been executed successfully.


# EX-17-NUMBERS-ARE-EVEN-OR-NOT

## AIM

Write a C program to check even or odd using simple if statement.

## ALGORITHM

```
1.Start
2.Declare an integer variable: number
3.Input a number from the user and store it in number
4.Check if the number is divisible by 2:
5.If number % 2 == 0, then
 → Print "Number is EVEN"
6.Else
 → Print "Number is ODD"
7.End
```

## PROGRAM

```
#include <stdio.h>

int main() {
    int number;
    
    
    scanf("%d", &number);
    
    if (number % 2 == 0) {
        printf("Number is EVEN\n");
    }
    else {
        printf("Number is ODD\n");
    }
    
    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/bd8258dc-3b25-4098-9fe7-6f859ff9c5eb)

           
## RESULT

Thus the program to check even or odd using simple if statement has been executed successfully


# EX-18-STRING-LOWERCASE-CONVERSION

## AIM

To write a the program to convert the given string into lowercase.

## ALGORITHM

```
1.Start
2.Declare a character array input[100] to store the string
3.Input a string using fgets() and store it in input
4.Remove the newline character (\n) from the string, if present:
 Find the position of \n using strcspn()
 Replace it with \0 (null character)
5.Traverse each character in the string using a loop:
 For each character input[i]:
 Convert it to lowercase using tolower()
 Store it back in input[i]
6.Output the modified string with a message:
 "Lower case String is: <string>"
7.End
```

## PROGRAM

```
#include <stdio.h>
#include <ctype.h>
#include <string.h>

int main() {
    char input[100];
    
    
    fgets(input, sizeof(input), stdin);
    
   
    input[strcspn(input, "\n")] = '\0';
    
   
    for (int i = 0; input[i]; i++) {
        input[i] = tolower(input[i]);
    }
    
    
    printf("Lower case String is:%s\n", input);
    
    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/6a714363-f4af-4778-87ee-72e2791c66b2)


## RESULT

Thus the program to convert the given string into lowercase has been executed successfully


# EX-19-COUNT-OF-WORDS-IN-A-STRING

## AIM

write a c program to length of a given  without using strlen  using Do-While loop.

## ALGORITHM

```
1.Start
2.Declare a character array str[100] to store the string
3.Declare an integer variable length and initialize it to 0
4.Input the string using fgets()
5.Use a do-while loop to calculate the string length:
 Check each character in the string:
 If the character is a newline '\n':
 Replace it with a null character '\0'
 Break the loop
 Else, increment length
 Continue until the character is '\0' (end of string)
6.Output the value of length (i.e., the number of characters before \n or \0)
7.End
```

## PROGRAM

```
#include <stdio.h>

int main() {
    char str[100];
    int length = 0;
    
    
    fgets(str, sizeof(str), stdin);
    
    
    do {
        if(str[length] == '\n') {
            str[length] = '\0'; 
            break;
        }
        length++;
    } while(str[length] != '\0');
    
    printf("%d\n", length);
    
    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/8c815380-7bd1-4c32-ba4a-03e3fc50f7cb)


## RESULT

Thus the program to count the total number of words in a given string using do While loop has been executed successfully.


# EX  -20 -COMPARING TWO STRINGS

## AIM

write a c program to compare without using strcmp  using For loop.

## ALGORITHM

```
1.Start
2.Declare two character arrays: str1[100] and str2[100]
3.Declare integer variables: i for indexing, and flag to track mismatch (initialize flag = 0)
4.Input two strings using fgets() for str1 and str2
5.Start a loop to compare both strings character by character:
 While str1[i] and str2[i] are not null (\0):
 If str1[i] != str2[i]:
 Set flag = 1 (indicates mismatch)
 If str1[i] > str2[i], print "str2 is Less than str1"
 Else, print "str1 is Less than str2"
 Break the loop
6.After the loop, check if flag == 0 (i.e., no mismatch so far):
 If both strings ended (str1[i] == '\0' && str2[i] == '\0'):
 Print "Both strings are Equal"
 Else if str1[i] == '\0' (i.e., str1 is shorter):
 Print "str1 is Less than str2"
 Else:
 Print "str2 is Less than str1"
7.End
```

## PROGRAM

```
#include <stdio.h>

int main() {
    char str1[100], str2[100];
    int i, flag = 0;

   
    fgets(str1, sizeof(str1), stdin);
    
    fgets(str2, sizeof(str2), stdin);

    for (i = 0; str1[i] != '\0' && str2[i] != '\0'; i++) {
        if (str1[i] != str2[i]) {
            flag = 1;
            if (str1[i] > str2[i]) {
                printf("str2 is Less than str1\n");
            } else {
                printf("str1 is Less than str2\n");
            }
            break;
        }
    }

    if (flag == 0) {
        if (str1[i] == '\0' && str2[i] == '\0') {
            printf("Both strings are Equal\n");
        } else if (str1[i] == '\0') {
            printf("str2 is Less than str1\n");
        } else {
            printf("str1 is Less than str2\n");
        }
    }

    return 0;
}
```

## OUTPUT
 ![image](https://github.com/user-attachments/assets/e112ccf4-1fa1-446b-bbf4-c4dff539a4e4)


## RESULT

Thus the C program to compare without using strcmp  using For loop has been executed successfully.

