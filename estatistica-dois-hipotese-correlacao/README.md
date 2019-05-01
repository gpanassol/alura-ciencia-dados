# Estatística II - Aprofundando em hipóteses e correlações

## Gerar lista de dados

```
x1 <- runif(30, 37.9, 38.8)
x2 <- runif(30, 36.0, 38.2)
```

## Hipóteses

H0 -> Hipotese nula
H0H -> Hipotese alternativa

Ao rodar um Teste de Hipótese em um programa, fique atento ao p-value. Se ele for menor que 0,05, ou seja 5%, descarte a Hipótese Nula e aceite a Hipótese Alternativa.

## Teste de hipóteses - Student Test

Para dados normalizados

```
x1 <- runif(30, 37.9, 38.8)
x2 <- runif(30, 36.0, 38.2)
> t.test(x1, x2)

        Welch Two Sample t-test

data:  x1 and x2
t = 10.166, df = 41.498, p-value = 7.872e-13
alternative hypothesis: true difference in means is not equal to 0
95 percent confidence interval:
 0.931044 1.392481
sample estimates:
mean of x mean of y
 38.33448  37.17272
```

## Teste de hipóteses - Wilcoxon

Para dados não normalizados

```
x1 <- runif(30, 37.9, 38.8)
x2 <- runif(30, 36.0, 38.2)
> wilcox.test(x1, x2)

        Wilcoxon rank sum test

data:  x1 and x2
W = 881, p-value = 3.529e-14
alternative hypothesis: true location shift is not equal to 0
```

## Dado pareados - paired

O teste <b>paired</b> significa que o estatístico colheu os dados da mesma amostra para compará-los.