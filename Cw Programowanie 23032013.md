Sam zrobilem zadanie numer 1, dla delta>0, trzeba także dla delta=0 i delta<0

```c

#include <stdio.h> 
#include <math.h>
int main() {
    double a,b,c,delta,x1,x2;
    printf("Podaj a:");
    scanf("%lf",&a);
    printf("Podaj b:");
    scanf("%lf",&b);
    printf("Podaj c:");
    scanf("%lf",&c);
    delta=b*b-4*a*c;
    
    if(delta>0){
                
     x1=(-b-sqrt(delta))/(2*a);
     x2=(-b+sqrt(delta))/(2*a);
     printf("x1=%lf\n",x1);
     printf("x2 =%lf\n",x2);
     }
     
     printf("Wyświetl pierwiastki trójmianu kwadratowego");
    
    getchar();             
    getchar();
    return 0;
}

```
