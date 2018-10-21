#include <stdio.h>
#include <stdlib.h>

//procedimento1 
void ordem (int i){
	i++;
	printf(" %i",i);
}
		

int main (){
	int soma = 0;
	int m = 2;
	int mmc = 1;
	int o;
	printf("numero de obstaculos: ");
	scanf("%i",&o);
	printf("\nFrequencia dos obstaculos em ordem crescente!");
	int f[o];
	int i=0;
 	for ( ; i < o; i++){
	printf("\nFrequencia do obstaculo");
	ordem(i);
	printf(": ");
	scanf("\n%i",&f[i]);	
	
	int x = 0;
		
			while (soma != o){
				if (f[i]%m != 0)
				{
					m=m+1;
					printf("\nm: %i",m);
				}
			else
				{
					mmc=mmc*m;
					printf("\nmmc: %i",mmc);

					f[i]=f[i]/m;
					x = f[i];
					printf("\nf: %i",f[i]);	
					if (f[i] == 1)
					break;
				}	
			
				
			soma = soma + x;	
			printf("\nsoma: %i",soma);
		
	
	}	
										
											
	}
	
					printf("\nMenor instante de tempo: %i",mmc);	
					
return 0;			
}
