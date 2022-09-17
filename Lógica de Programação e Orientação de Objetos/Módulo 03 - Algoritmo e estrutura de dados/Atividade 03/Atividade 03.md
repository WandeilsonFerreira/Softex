# Softex – Atividade 01

###  Crie um vetor com ponteiros utilizando alocação dinâmica na linguagem C, que:

- use a função realloc;
- use a função sizeof;
- que tenha tamanho 22 de vetor;
- depois libere o bloco utilizando a função free.

```
<C>  
#include <stdio.h>
#include <stdlib.h> 

int main(void)
{
  int i, tam = 22, *vet;  
  vet = (int *) malloc(5 * sizeof(int)); //Alocação do primeiro endereço de memória e reservando 5 espaços.
  vet = (int *) realloc(vet, tam * sizeof(int)); //Realocando o endereço de memória e reservando os espaços.

   if(vet){
        printf("Memoria alocada com sucesso!\n");
        for(i = 0; i < tam; i++)
            *(vet + i) = rand() % 100;

        for(i = 0; i < tam; i++)
            printf("%d ", *(vet + i));
        printf("\n");
    }
    else{
        printf("Erro ao alocar memoria!\n");
    }
    free(vet);
    return 0;
}
 
 
```
