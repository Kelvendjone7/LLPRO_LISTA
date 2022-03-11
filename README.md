# LLPRO_LISTA
#include <stdio.h>
#include <stdlib.h> 
#include <locale.h>

int peso_ideal(float altura, int sexo) {
	float peso;
	if(sexo == 0) {
	    peso = (72.7 * altura)- 58;
	    printf("\n\tSeu peso ideal é: %.2f Kg", peso);
  }else if(sexo == 1) {
    	peso = (62.1 * altura) - 44.7;
    	printf("\n\tSeu peso ideal é: %.2f Kg", peso);
  }
    return 0;  
}

int main() {
  setlocale(LC_ALL, "Portuguese_Brazil");
  int sexo;
	float alt;
    
  printf("\t\tINFORME SEUS DADOS\n");
    
	printf("\nDigite a sua altura: ");
	scanf("%f", &alt);
	
	printf("Digite o seu sexo: (MASCULINO - 0) e (FEMININO - 1): ");
	scanf("%d", &sexo);
	
  peso_ideal(alt, sexo);
    
return 0;

}
