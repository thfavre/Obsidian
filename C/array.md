#C
Subject linked to [[pointer]]

## Concept :
```C
int tab[3]  // demande au programme d'allouer 3 int sur la stack
```
tab est un pointeur sur int possedant l'adresse du premier int

```C
int tab[3];
tab[0] = 42;
printf("%d", *tab);  // 42
```

```C
int tab[3];
tab[1] = 777;
printf("%d", *(tab+1));  // 777
```
```C
tab[1] == *(tab + 1)
tab[n] == *(tab +n)
```



## String
 ![[string]]