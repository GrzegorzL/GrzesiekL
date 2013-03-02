#Wyklady z Jezyka Programowania notatki od Sylwka

###Sobota 02.03.2013 godz. 8.30               

## Podstawowy szkielet programu w C++ - Ćwiczenie pierwsze

```c
#include <stdio.h> // .h - rozszerzenie plika naglówkowego  

int main () {
    int a,b;
    a=3;
    b=7;
    printf("Wynik mnozenia to %d", a*b);
    getchar();  // pobierz znak z klawiatury
    return 0;
}
```   
***

## Ćwiczenie 2 - dodawanie, odejmowanie i dzielenie

```c
#include <stdio.h>

int main () {
    int a,b;
    a=3;
    b=7;
    printf("%d*%d=%d\n",a,b,a*b); // wyświetla koljeny argument, który jest liczbą całkowitą, a,b oraz wynik mnożenia tych liczb
    printf("%d+%d=%d\n",a,b,a+b);
    printf("%d-%d=%d\n",a,b,a-b);
    printf("%d/%d=%d",a,b,a/b);
    getchar();
    return 0;
}
```
***

## Ćwiczenie 3 - argument zmienno przecinkowy "lf", wykorzystanie "double"

```c
#include <stdio.h>

int main () {
    double a,b;
    a=3.0;
    b=7.0;
    printf("%lf * %lf=%lf\n",a,b,a*b); // wyświetla koljeny argument, który jest liczbą całkowitą, a,b oraz wynik mnożenia tych liczb
    printf("%lf + %lf=%lf\n",a,b,a+b);
    printf("%lf - %lf=%lf\n",a,b,a-b);
    printf("%lf / %lf=%lf",a,b,a/b); // lf- liczba zmienno przecinkowa, do 6 miejsc po przecinku , float- pamiętany w 4bajtach, double-8bajtów, 

    getchar();
    return 0;
}
```
***

## Ćwiczenie 4 - ograniczenie wyswietlanych miejsc po przecinku

```c
#include <stdio.h>

int main () {
    double a,b;
    a=3.0;
    b=7.0;
    printf("%.0lf * %.0lf =%.0lf\n",a,b,a*b); // .0lf - wyświetla zero miejsc po przecinku
    printf("%.0lf + %.0lf =%.0lf\n",a,b,a+b);
    printf("%.0lf - %.0lf =%.0lf\n",a,b,a-b);
    printf("%.0lf / %.0lf =%.3lf",a,b,a/b); // lf- liczba zmienno przecinkowa, do 6 miejsc po przecinku , float- pamiętany w 4bajtach, double-8bajtów, 

    getchar();
    return 0;
}
```
***

## Ćwiczenie 5 - Oblicz pole i obwód kola z użyciem plika naglówkowego <math.h>

```c
#include <stdio.h>
#include <math.h>
int main () {
    double r;
    //const double pi=3,1415926;          //stały, M_PI zadeklarowane w pliku <math.h>
    printf("Podaj promien kola: ");
    scanf("%lf",&r);
    printf("Pole kola o promieniu %.0lf wynosi %lf\n",r,M_PI*r*r);
    printf("Obowd kola wynosi: %d * %lf * %lf = %lf ",2,M_PI,r, 2*M_PI*r );
    getchar(); getchar ();
    return 0;
}
```
***

Grzeska notki opisowe:


&r - ampersant - wskaznik do zmiennych
dwa getchart, jedno czeka, drugie czeka az wcisniemy enter

....idziemy dalej.............


Obliczenia w petli

Cwiczenie: przeliczanie stopni farenhajta na celsiusza

```c
#include <stdio.h>
int main () {
   int fahr,celcius;
   int lower,upper,step;
   lower=0;
   upper=300;
   step=20;
 fahr=lower;
  while(fahr<=upper){                                          //mniejsze  lub równe, nie moze być większe
  celcius=5*(fahr-32)/9;
  printf("%d\t%d\n",fahr,celcius);
  fahr=fahr+step;                               //w programowaniu są wykonywane rownoznaczne działania od lewej do prawej np.przy 
}                                               //a+b*c/d  -jak jest mnozenie i dzielenie to od lewej
                                                 //wzór który oblicza celsjusze
getchar();                              
getchar();
return 0;
}
```

..i to samo, ale zmienno przecinkowe, czyli dopisujemy double oraz np. po procentach lf i iloci po przecinku kropka i liczba np - .2
  albo ...%5.2lf - czyli rozmiar pola 5 i ilosc liczb po przecinku to 2
```c
#include <stdio.h>
int main () {
   double fahr,celcius;
   int lower,upper,step;
   lower=0;
   upper=300;
   step=20;
 fahr=lower;
  while(fahr<=upper){                                          //mniejsze  lub równe, nie moze być większe
  celcius=5*(fahr-32)/9;
  printf("%lf\t%lf\n",fahr,celcius);
  fahr=fahr+step;                               //w programowaniu są wykonywane rownoznaczne działania od lewej do prawej np.przy 
}                                               //a+b*c/d  -jak jest mnozenie i dzielenie to od lewej
                                                 //wzór który oblicza celsjusze
getchar();                              
getchar();
return 0;
}

```
....







