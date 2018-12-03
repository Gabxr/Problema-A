#include <stdlib.h>
#include <stdio.h>

		//cálculo do mmc
		
	int mmc (int n1, int n2){ 
	int mmc, x, y, z;
		y = n1;
		x = n2;
			
		do{
			z = y % x;
			y = x;
			x = z;
			} while (z != 0);
	
	mmc = (n1*n2)/y;
	return mmc;
	}

		//principal
	int main (){
	
		printf("Problema A - Tiro ao Alvo!\n");
		int n;
		int i=0;
		int a, f[50];
		scanf("%d",&n);
		a=1;
		
			for ( ; i<n;++i){
			scanf("%d",&f[i]);
			a = mmc (f[i], a);
			}
				
			if (n!=0)
{
			printf("\nMenor instante de tempo para atingir o alvo: ");
			printf("\n%d", a);
			}
			
return 0;
}
