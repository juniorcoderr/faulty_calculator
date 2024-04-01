# faulty_calculator
function faultyCalculator(num1, num2, operation) {
    let result;
    
    // Perform faulty operations
    switch (operation) {
        case '+':
            result = num1 - num2;
            break;
        case '-':
            result = num1 / num2;
            break;
        case '*':
            result = num1 + num2;
            break;
        case '/':
            result = num1 ** num2;
            break;
        default:
            return "Invalid operation!";
    }
    
    return result;
}

// Take input from the user
const num1 = parseFloat(prompt("Enter first number:"));
const num2 = parseFloat(prompt("Enter second number:"));
const operation = prompt("Enter the arithmetic operation (+, -, *, /):");

// Calculate and display the result
const result = faultyCalculator(num1, num2, operation);
console.log(`The result of ${num1} ${operation} ${num2} is: ${result}`);

