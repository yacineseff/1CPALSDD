# 1CPALSDD

#include <stdio.h>
#include <string.h>
#include <stdlib.h>
int NF(int n){

     return ( n>0) ? n*NF(n-1):1;

}

void remplir(int *t[][10],int x ){  //  i set 10 to avoid overflow
for (int i=0;i<x;i++){
    for (int j=0;j<=i;j++) {
        t[i][j]=NF(i)/(NF(j)* NF(i-j));
 printf("%d | ", t[i][j]);
    }
      putchar ('\n');

}

return 0;

}
int main() {
   int x ;

    printf("Entrez un nombre entier  :\n ");
    scanf("%d", &x);

    int tableau[x][10]; //

    remplir(tableau, x);

    return 0;
}
