# Maxima Cheatsheet

## Allgemein

```solve(gleichung, x)``` -> Gleichungen bzw. Gleichungssysteme lösen

```subst(x=wert, funktion)``` -> Wert für x in einer Funktion einsetzen

```find_root(funktion=wert, x, a, b)``` -> Um x in dem Intervall [a; b] an der Stelle zu finden wo der Funktionswert einem bestimmten Wert entspricht

```realroots(funktion=wert)``` -> Um x an der Stelle zu finden wo der Funktionswert einem bestimmten Wert entspricht

```wxplot2d(funktion, [x, a, b])``` -> Um Funktion mit der Variable x in einem Intervall [a; b] zu plotten

```wxplot3d(funktion, [x, min, max], [y, min, max])``` -> Um Funktion in 3D-Raum zu plotten

```abs(wert)``` -> Um den Absolutwert eines Wertes zu finden

```limit(function, var, a)``` -> Grenzwert 



## Integral- und Differentialrechnung

```diff(funktion, variable, wieOft)``` -> Ableiten

```integrate(funktion, variable, untereGrenze, obereGrenze)``` -> Integrieren (Grenzen sind optional)

```romberg(funktion, variable, untereGrenze, obereGrenze)``` -> Integrieren wenn ```integrate()``` nicht funktioniert

## Regression

```matrix([a, b], [c, d])``` -> Matrix 

```lsquares_estimates(Matrix, [x, y], funktion, [a, b])``` -> Regression mit Funktion der Wahl, [a, b] sind die 
Koeffizienten der Funktion, die herausgefunden werden sollen. Davor ```load(lsquares)```

```simple_linear_regression(Matrix)``` -> Lineare Regression


## Differentialgleichungen

```ode2(DGL, dependantVar, independantVar)``` -> Um allgemeine Lösung für eine DGL auszurechnen

```ic1(allgLösung, x=wert, y=wert)``` -> Für spezielle Lösung einer DGL

```expand()``` -> Lösung erweitern


## Zahlentheorie, Matrizenrechnung, Vektoren

```mod(a, m)``` -> Modulo

```matrix([a, b], [c, d])``` -> Matrix

```determinant(Matrix)``` -> Determinante 

```transpose(Matrix)``` -> Matrix transponieren

```A.B``` -> Multiplikation von Matrix A und Matrix B

```invert(Matrix)``` -> Matrix invertieren

```[a, b]``` -> Vektor

```[a, b].[c, d]``` -> Vektoren multiplizieren

```express(a~b)``` -> Kreuzprodukt, davor ```load(vect)```


## Finanzmathematik

```sum(expression, var, begin, end)``` -> Summe 

```makelist(expression, var, begin, end``` -> Glieder der Folge

```taylor(expression, x, Ort, Ordnung)``` -> Taylorreihe 

## Statistik

```[a, b, c, d]``` -> Liste

```sort(list)``` -> sortiert Liste

```mean(list)``` -> Mittelwert

```median(list)``` -> Median

```quantile(list, p)``` -> Quantil einer Liste

```var(list), var1(list)``` -> Varianz einer Liste 

```std(list), std1(list)``` -> Standardabweichung

```range(list)``` -> Spannweite

```qrange(list)``` -> Interquartilsdistanz

```factorial(n), n!``` -> n-Fakultät

```binomial(n, k)``` -> Binomialkoeffizient


## Stochastik

```load(distrib)``` -> Vor allen der Funktionen

```pdf_binomial(x, werte_gesamt, wahrscheinlichkeit)``` -> Wahrscheinlichkeitsfunktion

```cdf_binomial(x, werte_gesamt, wahrscheinlichkeit)``` -> Verteilungsfunktion

```pdf_normal(x, erwartungswert, std)``` -> Dichtefunktion

```cdf_normal(x, erwartungswert, std)``` -> Verteilungsfunktion

```quantile_normal(quantil, erwartungswert, std)``` -> Quantil

```quantile_student(quantil, n)``` -> Quantil 