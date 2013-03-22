Cw.3 Wczytaj n liczb i wyswietl ich sume i srednia arytmetyczna

```

# include <stdio.h>
int main () {
    int n, i;
    double x, suma=0.0, srednia;
    do     {
    printf("Podaj ilosc liczb (co najmniej 1):");
    scanf("%d", &n);
    }
    while(n<1);

    for(i=1;i<=n;i++) {
                     printf("Podaj %d liczbe:", i);
                     scanf("%lf", &x);
                     suma=suma+x;
                     }
    srednia=suma/n;
    printf("Suma podanych %d liczb wynosi: %.1lf \n", n, suma);
    printf("Srednia z podanych %d liczb wynosi: %.1lf", n,srednia);
    getchar();
    getchar();
    return 0;
}

```
Cw 4 
