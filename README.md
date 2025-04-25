#include <iostream>
using namespace std;

// Function prototypes
float add(float x, float y);
float subtract(float x, float y);
float multiply(float x, float y);
float divide(float x, float y);

int main() {
    float num1, num2;
    int choice;

    cout << "Select operation:" << endl;
    cout << "1. Add" << endl;
    cout << "2. Subtract" << endl;
    cout << "3. Multiply" << endl;
    cout << "4. Divide" << endl;

    cout << "Enter choice (1/2/3/4): ";
    cin >> choice;

    cout << "Enter first number: ";
    cin >> num1;
    cout << "Enter second number: ";
    cin >> num2;

    switch (choice) {
        case 1:
            cout << num1 << " + " << num2 << " = " << add(num1, num2) << endl;
            break;
        case 2:
            cout << num1 << " - " << num2 << " = " << subtract(num1, num2) << endl;
            break;
        case 3:
            cout << num1 << " * " << num2 << " = " << multiply(num1, num2) << endl;
            break;
        case 4:
            if (num2 != 0) {
                cout << num1 << " / " << num2 << " = " << divide(num1, num2) << endl;
            } else {
                cout << "Error! Division by zero." << endl;
            }
            break;
        default:
            cout << "Invalid input" << endl;
            break;
    }

    return 0;
}

// Function definitions
float add(float x, float y) {
    return x + y;
}

float subtract(float x, float y) {
    return x - y;
}

float multiply(float x, float y) {
    return x * y;
}

float divide(float x, float y) {
    return x / y;
}
