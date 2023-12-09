Write a  basic c program to check whether a string is in password vaildation.


    #include <stdio.h>
    #include <stdbool.h>

    bool isPasswordValid(char password[]) {
    // Check if the length of the password is at least 8 characters
    if (strlen(password) < 8) {
        return false;
    }

    // Check if the password contains at least one digit
    bool hasDigit = false;
    for (int i = 0; password[i] != '\0'; i++) {
        if (isdigit(password[i])) {
            hasDigit = true;
            break;
        }
    }

    // Check if the password contains at least one uppercase letter
    bool hasUppercase = false;
    for (int i = 0; password[i] != '\0'; i++) {
        if (isupper(password[i])) {
            hasUppercase = true;
            break;
        }
    }

    // Check if the password contains at least one lowercase letter
    bool hasLowercase = false;
    for (int i = 0; password[i] != '\0'; i++) {
        if (islower(password[i])) {
            hasLowercase = true;
            break;
        }
    }

    // Check if the password meets all criteria
    return (hasDigit && hasUppercase && hasLowercase);
    }

    int main() {
    char password[100];

    // Get password input from the user
    printf("Enter a password: ");
    scanf("%s", password);

    // Check if the password is valid
    if (isPasswordValid(password)) {
        printf("Password is valid.\n");
    } else {
        printf("Password is not valid.\n");
    }

    return 0;
}


Output of the program:


![image](https://github.com/AklavyaSangra/Assignment/assets/146859465/8008d5e5-326f-43d6-8de7-1f6debb7e475) 


![image](https://github.com/AklavyaSangra/Assignment/assets/146859465/025f733d-997a-444e-897a-9da18fd24721)



