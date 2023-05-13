#include <stdio.h>
#include <math.h>

int main()
{
    double num1, num2, result;
    char operator;

    printf("Enter an operator (+, -, *, /, ^, s, c, t, l): ");
    scanf("%c", &operator);

    switch(operator)
    {
        case '+':
            printf("Enter two numbers to add: ");
            scanf("%lf %lf", &num1, &num2);
            result = num1 + num2;
            printf("%.2lf + %.2lf = %.2lf", num1, num2, result);
            break;

        case '-':
            printf("Enter two numbers to subtract: ");
            scanf("%lf %lf", &num1, &num2);
            result = num1 - num2;
            printf("%.2lf - %.2lf = %.2lf", num1, num2, result);
            break;

        case '*':
            printf("Enter two numbers to multiply: ");
            scanf("%lf %lf", &num1, &num2);
            result = num1 * num2;
            printf("%.2lf * %.2lf = %.2lf", num1, num2, result);
            break;

        case '/':
            printf("Enter two numbers to divide: ");
            scanf("%lf %lf", &num1, &num2);
            if(num2 == 0)
            {
                printf("Error: Cannot divide by zero");
            }
            else
            {
                result = num1 / num2;
                printf("%.2lf / %.2lf = %.2lf", num1, num2, result);
            }
            break;

        case '^':
            printf("Enter two numbers to find the power: ");
            scanf("%lf %lf", &num1, &num2);
            result = pow(num1, num2);
            printf("%.2lf ^ %.2lf = %.2lf", num1, num2, result);
            break;

        case 's':
            printf("Enter a number to find the sine: ");
            scanf("%lf", &num1);
            result = sin(num1);
            printf("sin(%.2lf) = %.2lf", num1, result);
            break;

        case 'c':
            printf("Enter a number to find the cosine: ");
            scanf("%lf", &num1);
            result = cos(num1);
            printf("cos(%.2lf) = %.2lf", num1, result);
            break;

        case 't':
            printf("Enter a number to find the tangent: ");
            scanf("%lf", &num1);
            result = tan(num1);
            printf("tan(%.2lf) = %.2lf", num1, result);
            break;

        case 'l':
            printf("Enter a number to find the natural logarithm: ");
            scanf("%lf", &num1);
            result = log(num1);
            printf("ln(%.2lf) = %.2lf", num1, result);
            break;

        default:
            printf("Error: Invalid operator");
            break;
    }

    return 0;
}
