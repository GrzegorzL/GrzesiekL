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
OD SYLWESTRA

## Cwiczenie 17 - Napisz program liczacy pierwiastki trojmianu kwadratowego: a*x^2+b*x+c=0.

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
    printf("Delta= %.0lf*%.0lf-%d*%.0lf*%.0lf= %.3lf\n\n",b,b,4,a,c,b*b-4*a*c);
    
   if (delta>0) {
                x1=(-b-sqrt(delta))/(2*a);
                x2=(-b+sqrt(delta))/(2*a);
                printf("x1 = %.2lf \n",x1);
                printf("x2 = %.2lf\n\n", x2);
                printf("Delta wieksza od zero!!!");
               
    
}
    else if (delta==0) {
                x1=x2=(-b)/(2*a);
                printf("x1 = %.0lf \n",x1);
                printf("x2 = %.0lf\n\n", x2);
                printf("Delta rowna sie zero!!");
}
  
   else {
           printf("Blad nie ma rozwiazania");
}

                   
                 
                 
    getchar();
    getchar();
    return 0;
}
```

***



