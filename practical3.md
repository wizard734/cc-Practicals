public class Calculator {
    public static Integer calculate(Integer num1, Integer num2, String operator) {
        if (operator == '+') return num1 + num2;
        else if (operator == '-') return num1 - num2;
        else if (operator == '*') return num1 * num2;
        else if (operator == '/') {
            if (num2 == 0) throw new MathException('Division by zero');
            return num1 / num2; // Integer division (truncates decimal)
        }
        else throw new IllegalArgumentException('Invalid operator: ' + operator);
    }
}

System.debug(Calculator.calculate(10, 5, '+')); // 15
System.debug(Calculator.calculate(10, 3, '/')); // 3 (integer division)
