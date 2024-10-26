# ift-1004-a2024-qem2-JOATH1
Ce repository contient les réponses au questionnaire Exercices du module 2.

## Question 1
Donnez les valeurs des variables a, b et c après l'exécution du pseudo-code suivant:
```
a <- 8
b <- -a
c <- a + b
```
```
Trace:
a
8
b
-8
a + b
8 + (-8)
0

Réponse:
Après l'exécution du pseudo-code:
- la variable a est égale à 8;
- la variable b est égale à -8;
- la variable c est égale à 0.
```

## Question 2
Donnez les valeurs des variables a, b et c après l'exécution du pseudo-code suivant:
```
a <- 5
b <- 10 + 2
c <- a + b - 3
b <- a
```
```
Trace:
a
5
b
10 + 2
12
c
a + b - 3
5 + 12 - 3
17 - 3
14

Réponse:
Après l'exécution du pseudo-code:
- la variable a est égale à 5;
- la variable b est égale à 12;
- la variable c est égale à 14.
```

## Question 3
Donnez les valeurs des variables a, b et c après l'exécution du pseudo-code suivant:
```
a <- 1
b <- a
a <- a + a
a <- a * a * a
c <- a + b
```
```
Trace:
a
1
b
a
1
a
a + a
1 + 1
2
a
a * a * a
2 * 2 * 2
4 * 2
8
c
a + b
8 + 1
9

Réponse:
Après l'exécution du pseudo-code:
- la variable a est égale à 8;
- la variable b est égale à 1;
- la variable c est égale à 9.
```

## Question 4
Donnez les types des variables a, b et c après l'exécution du pseudo-code suivant:
```
Trace:
a
"programmation"
type(a)
str
b
3.0
type(b)
float
c
​3
type(c)
int

Réponse:
Après l'exécution du pseudo-code:
- la variable a est de type chaîne de caractères;
- la variable b est de type réel;
- la variable c est de type entier.
```

## Question 5
Donnez les types des variables a, b et c après l'exécution du pseudo-code suivant:
```
a <- 3.1416
b <- 2
c <- a * b
```
```
Trace:
a
3.1416
type(a)
float
b
2
type(b)
int
c
3.1416 * 2
3.1416 * 2.0
6.2832
type(c)
float

Réponse:
Après l'exécution du pseudo-code: 
- la variable a est de type réel;
- la variable b est de type entier;
- la variable c est de type réel.

Explication:
La variable c contient le résultat d'une multiplication entre une variable de type réel et d'une variable de type entier.

{
Python fully supports mixed arithmetic: when a binary arithmetic operator has operands of different numeric types, the operand with the “narrower” type is widened to that of the other, where integer is narrower than floating point, which is narrower than complex.
}
Article: Numeric Types — int, float, complex
Source: https://docs.python.org/3/library/stdtypes.html#numeric-types-int-float-complex

Durant l'exécution de la multiplication, la variable de type int est "convertie" en réel afin
de ramener les opérandes de la mutiplication à un même type,
sans qu'il y est de perte de la valeur initiale lors de la conversion.

Le résultat de cette conversion se résume à la multiplication entre deux variables de type réel.
```

## Question 6
Donnez les types des variables a, b et c après l'exécution du pseudo-code suivant:
```
a <- 3.0
b <- 2
c <- a + b
```
```
Trace:
a
3.0
type(a)
float
b
2
type(b)
int
c
a + b
3.0 + 2
3.0 + 2.0
5.0

Réponse:
Après l'exécution du pseudo-code: 
- la variable a est de type réel;
- la variable b est de type entier;
- la variable c est de type réel.

Explication:
La variable c contient le résultat d'une multiplication entre une variable de type réel et d'une variable de type entier.

{
Python fully supports mixed arithmetic: when a binary arithmetic operator has operands of different numeric types, the operand with the “narrower” type is widened to that of the other, where integer is narrower than floating point, which is narrower than complex.
}
Article: Numeric Types — int, float, complex
Source: https://docs.python.org/3/library/stdtypes.html#numeric-types-int-float-complex

Durant l'exécution de l'addition (ou de toute autre opération arthimétique), la variable de type int est "convertie" en réel afin
de ramener les opérandes de l'addition (ou de toute autre opération arthimétique) à un même type, 
sans qu'il y est de perte de la valeur initiale lors de la conversion.

Le résultat de cette conversion se résume à l'addtion (ou de toute autre opération arthimétique) entre deux variables de type réel.
```
Ceci est un test.