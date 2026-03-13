#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int length, i;
    
    char characters[] = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()";
    
    int charSize = sizeof(characters) - 1;

    printf("Enter password length: ");
    scanf("%d", &length);

    srand(time(NULL));

    printf("Generated Password: ");

    for(i = 0; i < length; i++) {
        int index = rand() % charSize;
        printf("%c", characters[index]);
    }

    printf("\n");

    return 0;
}
