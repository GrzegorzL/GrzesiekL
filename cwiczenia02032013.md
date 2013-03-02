Sobota 02.03.2013 cwieczenia  zProgramowania w C

#include<studio.h>
```c
int main(){
int a,b
a=3;
b=7;
printf("wynik mnozenia to %d",a*b)

```
Mnozenie

#include<studio.h>
```c
int main(){
int a,b
a=3;
b=7;
printf("%d*%d=%d",a,b,a*b);
```

liczby zmienno przecinkowe - float, double w bajtach

%f - liczby zmienno przecinkowe, zeby wuyswietlicz wynik dzielenia po przecinku, l - liczba

to double a=3, b=7;

```c
#include,studio.h>
int main(){
int a,b;
double a=3,b=7;
printf("%.0lf+%.0lf=&.0lf\n", a,b,a+b);
}
```

Oblicz pole kola o promieniu

<math.h>  - ma dokladne Pi - stala M_PI

```c
#include <stdio.h>
#include<math.h>
int main () {
double r;
puts("podaj promien kola:");
scanf("%lf",&r);
printf("Pole kola o promieniu %lf wynosi %lf",r,M_PI*r*r);
getchar();
getchar();
return 0;
}
