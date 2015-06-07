# moje-notatki-z-programowania
zad .1 
Napisz program liczacy pierwiastki trjmianu kwadratowego: a*x^2+b*x+c=0.
Rozwiazanie:
#include<stdio.h>
#include<math.h>
int main(){
	double a,b,c,delta,x,x1,x2;
	printf("Podaj liczbe a=\n");
	scanf("%lf",&a);
		printf("Podaj liczbe b=\n");
	scanf("%lf",&b);
		printf("Podaj liczbe c=\n");
	scanf("%lf",&c);
	{
		delta=b*b-4*a*c;
		if (delta<0)
		{
			printf("Brak rozwiazan rzeczywistych\n");
			getchar();
		if(delta==0)
		{
			x=-b/(2.0*a);
			printf("Pierwiastek podwojny:%lf\n",x);
			getchar();		
		}
		if(delta>0)
		{
			x1=(-b-sqrt(delta))/(2.0*a);
			x2=(-b+sqrt(delta))/(2.0*a);
			printf("Rownanie ma dwa pierwiastki:%lf\n %lf\n",x1,x2);
			getchar();		}
		}
		
	}
	return 0;
}
Zad.2 
Znajdz liczbyo tej wlasnosci, ze suma dzielnikow wlasciwch liczby jest rowna zadanej liczbie, np 6=1+2+3.
Sa to tak zwane liczby doskonale.
Roziwazanie:
#include<stdio.h>
int main(){

int dzielnik,liczba,suma;
for (liczba=2;liczba<10000;liczba++){

suma=0;

for(dzielnik=1;dzielnik<liczba;dzielnik++){
	if(liczba%dzielnik==0){
	suma=suma+dzielnik;
}
}
	if(suma==liczba){
	printf("\n Liczba doskonala %d=1",liczba);
		for(dzielnik=2;dzielnik<liczba;dzielnik++){
			if(liczba%dzielnik==0){
				printf("+%d",dzielnik);
			}
	}
}
}
return 0;
}
