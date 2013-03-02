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

Cwiczenia  - DEFINE i petla for
```c
#include <stdio.h>
#define LOWER 0                   // stale preprocesora jezyka C, nie moze byc na koncu srednika,wszystkie wystapienia slowa lower zamien na o, 
#define UPPER 300                    // wszystkie wystapienia upper zamien na 300, a step na 20 - działa jak automat, bierze i zastepuje i tyle!!!!
#define STEP 20

int main () {
  int fahr;
  for(fahr=LOWER;fahr<=UPPER;fahr=fahr+STEP)                    // 3 czesci - za fahr podstawiamy LOWEr, otem sprawdmy czy LOWER jest mneijsze/równe - 
  printf("%3d %6.1lf\n",fahr,(5.0/9.0)*(fahr-32));                                                              // jak jest to wracamy i zminna far zwiekszana o 20, i petla jes tykonywana, i tak dalej az fahr bedzie wiekszy od upper
                                                               // warunek3 po kazdym przebiegu petli zmieniamy, za instrukacja for nie ma srednika
                                                               // tu jest koniec instrukcji for - srednik, 
getchar();                              
return 0;
}
```

<h2>Ciag Fibonaciego - liczy sume dwóch kolejnych miejsc z ciagu

czyli suma z miejsca 1 i 2 jest w miejscu 3, w miejscu 4 jest liczba z sumy 2 i 3...itd  
komentarz: petla wykonana raz i dopiero potem sprawdzony warunek, i wiecej razy jesli zostanie speniony - to zasady petli do/while
petla do/while mozna zabezpieczyc sie przed blednymi danymi wprowadzonycmi przez uzytkownika
podswiamy,  apotem petla while
++1  to zwieksz o 1 po wykonaniu instrukcji,
i liczymy wyraz który jest suma dwóch poprzednich



```c
#include <stdio.h>
 int main ()
{                                    /*petla do/while - ciagi Fibonaciego u1=1, u2=2, Un=Un-1 +Un-2 dla n>2, pokazuje wyraz w ciagu, i suma dwóch przed szukanym*/
  int u1,u2,u3;
    int n;
    int i;
  do
    { 
      printf("Podaj numer wyrazu(co najmniej 3):");
      scanf ("%d",&n);  
    }
  while (n<3);
  
  u2=u1=1;
  i=2;
  while (i++<n)
 { u3=u1+u2;
 u1=u2;
 u2=u3;
}
printf ("Wyraz o numerze %d ma wartosc %d", n,u3); 
 
getchar();   
getchar();                           
return 0;
}
```

<h2>Cwiczenie na robienie trojkata z wykorzystaniem petli for

Komentarz: stala nazywa sie znak, bo znaki umiesczamy w pojedynczym apostrofie
  petla for prebiega przez wszystkie wiersze, zwiekszaj liczbe wierszy o 1, liczba odstepów, to ile spacji wyswietlic na poczatku kazdej kolejnki
  putchar - funkcja ktora wyswietla na ekran jeden znaczek, nastepnie petla ktora wyswietla znaczki, tj. dwa razy numer wiersza plus jeden
  po zakonczeniu wyswietlania wszystklich gwiazdek, wyswietlamy nowa linie (\n) w pojedynczym apostrofie
  lbwier - liczba wierszy, lw- liczba wierszy, lodst - liczba odstepów

```c
#include <stdio.h>
#define znak '*'
 int main ()
{ int lbwier;
  int lw;
  int lodst;
  int j;
  puts("Ile wierszy?");
  scanf("%d",&lbwier);
  for (lw=0;lw<lbwier;lw++)
  {
  lodst=lbwier-lw-1;
  for (j=0; j<lodst; j++) putchar(' ');
  for (j=0; j<2*lw+1; j++) putchar(znak);
  putchar('\n');
  }                                
getchar();   
getchar();                           
return 0;
}
```
<h2> Zadania z kartki

1.Wypisz liczby cakowite od 0 do 23 za pomoca petli for, while i do-while

<ol> Petla for
```c
#include <stdio.h>
int main(){
int i;
for(i=0;i<=23;i++)
printf("%d,",i);
getchar();
return 0;
}
```
<ol> Petla while
```c
#include <stdio.h>
int main(){
int i;
i=0;
while(i<=23){
printf("%d,",i);
i=i+1;
}
getchar();getchar();
return 0;
}
```

<ol> Petla do-while

```c
#include <stdio.h>
int main(){
int i=0;
do {
printf ("%d\n", i);    
n=n+1; 
}
while (i<23);
printf ("%d,", i);  
getchar ();
}
```
komentarz - trzy wspolne cechy: i=0, i-i+1, i<=23

2.Wypisz liczby od -3.5 do 7.5 z krokiem co 0.5 za pomoca petli for i while
