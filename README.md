#include <stdio.h>
#define FRU 100
int main(void){
int K[FRU][FRU],i, j, quant, linha, coluna, perm;
    scanf("%d",&quant);

    perm = 1;
    for(i=0; i<quant; i++){
        for(j=0; j<quant; j++){
            scanf("%d",&K[i][j]);

            if(!(K[i][j]>=0 && K[i][j]<=1))
            perm=0;
        }
    }


     for(i=0; i<quant && perm ==1; i++){
        linha=0;
        for(j=0; j<quant; j++){
        linha+=K[i][j];

        }
        if(linha!=1)
        perm=0;

    }

    for(j=0; j<quant && perm == 1; j++){
        coluna=0;
        for(i=0; i<quant; i++){
        coluna+=K[i][j];

        }
        if(coluna!=1)
        perm=0;
    }
    if(perm==1)
        printf("é permutação");
    else
        printf("Não é permutação");



return 0;
}
