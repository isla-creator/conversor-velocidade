

// Funções de #include <stdio.h>conversão
float kmh_para_ms(float velocidade) {
    return velocidade / 3.6;
}

float ms_para_kmh(float velocidade) {
    return velocidade * 3.6;
}

// Função principal
void unidades_de_velocidade() {
    int opcao;
    float velocidade, resultado;

    do {
        printf("\n******** Conversor de Unidades de Velocidade ********\n");
        printf("1. Km/h para m/s\n");
        printf("2. m/s para Km/h\n");
        printf("3. Sair\n");
        printf("Escolha uma opção: ");
        scanf("%d", &opcao);

        if (opcao == 1) {
            printf("Digite a velocidade em Km/h: ");
            scanf("%f", &velocidade);
            resultado = kmh_para_ms(velocidade);
            printf("%.2f Km/h é igual a %.2f m/s\n", velocidade, resultado);
        } else if (opcao == 2) {
            printf("Digite a velocidade em m/s: ");
            scanf("%f", &velocidade);
            resultado = ms_para_kmh(velocidade);
            printf("%.2f m/s é igual a %.2f Km/h\n", velocidade, resultado);
        } else if (opcao == 3) {
            printf("Saindo...\n");
        } else {
            printf("Opção inválida. Tente novamente.\n");
        }
    } while (opcao != 3);
}

int main() {
    unidades_de_velocidade();
    return 0;
}
