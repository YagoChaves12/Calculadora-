#include <stdio.h>

int main() {
    int opcao;
    float num1, num2, resultado;

    printf("Calculadora Simples em C\n");
    printf("Escolha a operacao:\n");
    printf("1. Adicao\n");
    printf("2. Subtracao\n");
    printf("3. Multiplicacao\n");
    printf("4. Divisao\n");
    printf("Digite a opcao (1/2/3/4): ");
    scanf("%d", &opcao);

    printf("Digite o primeiro numero: ");
    scanf("%f", &num1);
    printf("Digite o segundo numero: ");
    scanf("%f", &num2);

    switch(opcao) {
        case 1:
            resultado = num1 + num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case 2:
            resultado = num1 - num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case 3:
            resultado = num1 * num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case 4:
            if(num2 != 0)
                resultado = num1 / num2;
            else {
                printf("Erro: divisao por zero!\n");
                return 1;
            }
            printf("Resultado: %.2f\n", resultado);
            break;
        default:
            printf("Opcao invalida!\n");
    }

    return 0;
}
