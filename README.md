#include <stdio.h>

// Definição da struct deve vir antes do uso 
struct Carta{

    char estado; 
    char codigo[10];
    char cidade[100];
    int populacao;
    float area;
    float pib;
    int pontosturisticos;
};

// Função para ler os dados da struct Carta

void lerCarta(struct Carta *c)
{

    printf("Digite o estado:");
    scanf("%c", &c->estado); 

    printf(" Digite o codigo:");
    scanf("%s", &c->codigo);

    printf(" Digite o nome da Cidade:");
    scanf("%[^\n]", &c->cidade);

    printf("Digite o número da populacao:");
    scanf("%d", &c->populacao);

    printf("Digite area da cidade:");
    scanf("%f", &c->area);

    printf("Digite o PIB:");
    scanf("%f", &c->pib);

    printf("Digite os Pontos Turístico:");
    scanf("%d", &c->pontosturisticos);
}
int main(){

    struct Carta carta1, carta2; // Agora 'carta' está completamente defindo antes de uso
    printf("Preencha os dados da Primeira carta:\n");
    lerCarta(&carta1);

    printf("Preencha os dados da Segunda Carta:\n");
    lerCarta(&carta2);

// Exibir os dados para conferir

    printf("\n--- Inormações da Primeira Carta ---\n");
    printf("Estado: %c\n", carta1.estado);
    printf("Código: %s\n", carta1.codigo);
    printf("Cidade: %s\n", carta1.cidade);
    printf("População: %d\n", carta1.populacao);
    printf("Área: %f\n", carta1.area);
    printf("PIB: %f\n", carta1.pib);
    printf("Pntos Turístico: %d\n", carta1.pontosturisticos);

    printf("\n--- Inormações da Segunda Carta ---\n");
    printf("Estado: %c\n", carta2.estado);
    printf("Código: %s\n", carta2.codigo);
    printf("Cidade: %s\n", carta2.cidade);
    printf("População: %d\n", carta2.populacao);
    printf("Área: %f\n", carta2.area);
    printf("PIB: %f\n", carta2.pib);
    printf("Pntos Turístico: %d\n", carta2.pontosturisticos);

    return 0;
    }
