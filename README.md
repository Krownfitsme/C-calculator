# C-calculator#include <iostream>
using namespace std;

// Function to perform addition
double add(double a, double b) {
  return a + b;
}

// Function to perform subtraction
double subtract(double a, double b) {
  return a - b;
}

// Function to perform multiplication
double multiply(double a, double b) {
  return a * b;
}

// Function to perform division
double divide(double a, double b) {
  if (b == 0) {
    cout << "Error: Cannot divide by zero" << endl;
    return 0;
  }
  return a / b;
}

int main() {
  char operatorSymbol;
  double num1, num2, result;

  cout << "Enter an operator (+, -, *, /): ";
  cin >> operatorSymbol;

  cout << "Enter the first number: ";
  cin >> num1;

  cout << "Enter the second number: ";
  cin >> num2;

  switch (operatorSymbol) {
    case '+':
      result = add(num1, num2);
      break;
    case '-':
      result = subtract(num1, num2);
      break;
    case '*':
      result = multiply(num1, num2);
      break;
    case '/':
      result = divide(num1, num2);
      break;
    default:
      cout << "Invalid operator" << endl;
      return 0;
  }

  cout << "Result: " << result << endl;

  return 0;
}
