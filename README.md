# -Calculadora-Simples
este é um projeto iniciante para uma calculadora de contas simples.
## 🛠️ Funcionalidades

- Adição ➕
- Subtração ➖
- Multiplicação ✖️
- Divisão ➗
- Limpar valores
- Interface simples e fácil de usar
''--------------------------------------------------''




#include <stdio.h>
#include <stdlib.h>

int main() {
    char operacao;
    double num1, num2, resultado;
    int continuar = 1;

    while (continuar) {
        // Menu
        printf("\n=== Calculadora Simples ===\n");
        printf("Escolha uma operação:\n");
        printf(" +  Adição\n");
        printf(" -  Subtração\n");
        printf(" *  Multiplicação\n");
        printf(" /  Divisão\n");
        printf(" c  Limpar valores\n");
        printf(" s  Sair\n");
        printf("Operação: ");
        scanf(" %c", &operacao);

        if (operacao == 's' || operacao == 'S') {
            printf("Saindo da calculadora...\n");
            break;
        }

        if (operacao == 'c' || operacao == 'C') {
            num1 = num2 = resultado = 0;
            printf("Valores limpos!\n");
            continue;
        }

        // Solicitar números
        printf("Digite o primeiro número: ");
        scanf("%lf", &num1);
        printf("Digite o segundo número: ");
        scanf("%lf", &num2);

        // Realizar operação
        switch (operacao) {
            case '+':
                resultado = num1 + num2;
                printf("Resultado: %.2lf\n", resultado);
                break;
            case '-':
                resultado = num1 - num2;
                printf("Resultado: %.2lf\n", resultado);
                break;
            case '*':
                resultado = num1 * num2;
                printf("Resultado: %.2lf\n", resultado);
                break;
            case '/':
                if (num2 == 0) {
                    printf("Erro: Divisão por zero!\n");
                } else {
                    resultado = num1 / num2;
                    printf("Resultado: %.2lf\n", resultado);
                }
                break;
            default:
                printf("Operação inválida!\n");
        }
    }

    return 0;
}
