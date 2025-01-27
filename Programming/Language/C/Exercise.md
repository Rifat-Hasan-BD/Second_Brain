# Chapter 1
## 1.17
```
#include <stdio.h>

// Function prototype
int string_length(const char *str);
char even_string_swap(char *str, double middle);
char odd_string_swap(char *str, double middle);

int main() {
    char str[] = "rifatt";
    int str_length = string_length(str); // Call the function
    
    double mid_length = (double) str_length / 2;

    // Check if length is odd or even
    if (mid_length == (int)mid_length) {
        //even string
        even_string_swap(str, mid_length);
    } else {
        //odd string
        odd_string_swap(str, mid_length);
    }

    return 0;
}

// Function definition
int string_length(const char *str) {
    int count = 0;
    while (str[count] != '\0') {
        count++;
    }
    return count;
}

char even_string_swap(char *str, double middle) {
    int mid_length = (int) middle;
    int full_length = (mid_length * 2) - 1;

    for(int i = 0; i < mid_length; i++) {
        char right_side = str[i];
        char left_side = str[full_length - i];

        // Swap characters
        str[i] = left_side;
        str[full_length - i] = right_side;
        // printf("Right side: %c Left side: %c\n", right_side, left_side);
    }

    printf("New string is :%s", str);
}

char odd_string_swap(char *str, double middle) {
    int convert_mid_length = (int) middle;
    int mid_length = convert_mid_length + 1;
    int full_length = convert_mid_length * 2;

    for(int i = 0; i < mid_length; i++) {
        char right_side = str[i];
        char left_side = str[full_length - i];

        // Swap characters
        str[i] = left_side;
        str[full_length - i] = right_side;
    }

    printf("New string is :%s", str);
}
```
