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
### Solutionnaire
```
a = 8
b = -8
c = 0
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
b # Explication de l'erreur de la valeur de la variable b : Trace incomplète
5 # Explication de l'erreur de la valeur de la variable b : Trace incomplète

Réponse:
Après l'exécution du pseudo-code:
- la variable a est égale à 5;
- la variable b est égale à 12;
- la variable c est égale à 14.
```
### Solutionnaire
```
a = 5
b = 5
c = 14
b vaut 12 lors du calcul de la valeur de c, mais est réassigné à 5 par la suite.
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
a = 8
b = 1
c = 9
b prend la valeur initiale de a, par la suite a devient 2 (1+1), puis 8 (2*2*2), mais b ne change plus.
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
### Solutionnaire
```
a = 8
b = 1
c = 9
b prend la valeur initiale de a, par la suite a devient 2 (1+1), puis 8 (2*2*2), mais b ne change plus.
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
3
type(c)
int

Réponse:
Après l'exécution du pseudo-code:
- la variable a est de type chaîne de caractères;
- la variable b est de type réel;
- la variable c est de type entier.
```
### Solutionnaire
```
a: chaîne de caractères
b: réel
c: entier
Même si b et c ont mathématiquement la même valeur, leur représentation interne en mémoire diffère!
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
### Solutionnaire
```
a: réel
b: entier
c: réel
Comme le type réel admet plus de possibilités, c'est cela qu'on obtient en faisant une opération entre entiers et réels.
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
### Solutionnaire
```
a: réel
b: entier
c: réel
c provient d'une opération entre entiers et réels, donc on obtient bien un réel (5.0) même si ça ne serait pas forcément nécessaire!
```
## Question 7
Soit la fonction mathématique y = 2x+1, où x et y sont réels. Remplissez ce programme trouvant le y associé à un x en remplaçant la ligne # par votre code:
```
x <- Demander("x:")
#
Afficher("y = ", y)
```
```
x <- Demander("x:")

y = (2 * x) + 1

Afficher("y = ", y)
```
### Solutionnaire
```
x <- Demander("x:")
y <- 2*x + 1
Afficher("y = ", y)
```
## Question 8
Soit la fonction mathématique y = 2x+1, où x et y sont réels. Remplissez ce programme trouvant le x associé à un y en remplaçant la ligne # par votre code:
```
y <- Demander("y:")
#
Afficher("x = ", x)
```
```
y <- Demander("y:")
x = (y - 1) / 2
Afficher("x = ", x)

Article: La résolution algébrique d'une inéquation
Source: https://www.alloprof.qc.ca/fr/eleves/bv/mathematiques/la-resolution-algebrique-d-une-inequation-m1458

En effectuant la trace de l'algorithme,
y
9
type(y)
int
x
(y - 1) / 2
(9 - 1) / 2
8 / 2
4.0
type(x)
float

on se rend compte que le quotient de la division est de type réel
alors que les opérandes de la division sont de type entier. 

{
The / (division) and // (floor division) operators yield the quotient of their arguments. 
The numeric arguments are first converted to a common type. 
Division of integers yields a float, 
while floor division of integers results in an integer; 
the result is that of mathematical division with the ‘floor’ function applied to the result. 
Division by zero raises the ZeroDivisionError exception.
}
Article: 6.7. Binary arithmetic operations
Source: https://docs.python.org/3/reference/expressions.html#binary-arithmetic-operations

L'explication à ce comportement est que, 
dans Python, 
la division d'entier génère un résulat de type entier.
```
### Solutionnaire
```
y <- Demander("y:")
x <- (y - 1) / 2
Afficher("x = ", x)
ou

y <- Demander("y:")
z <- y - 1
x <- z / 2
Afficher("x = ", x)
Notez bien que quelque chose comme 2*x + 1 <- y ne serait pas permis. La partie gauche doit toujours être un nom de variable seul.
```
## Question 9
Remplissez ce programme trouvant la somme de deux nombres en remplaçant la ligne # par votre code:
```
nombre_1 <- Demander("Un premier nombre:")
nombre_2 <- Demander("Un deuxième nombre:")
#
Afficher("Le somme est:", somme)
```
```
nombre_1 <- Demander("Un premier nombre:")
nombre_2 <- Demander("Un deuxième nombre:")
somme = nombre_1 + nombre_2
Afficher("Le somme est:", somme)
```
### Solutionnaire
```
nombre_1 <- Demander("Un premier nombre:")
nombre_2 <- Demander("Un deuxième nombre:")
somme <- nombre_1 + nombre_2
Afficher("Le somme est:", somme)
```
## Question 10
Quel entier obtiendra-t-on suite à l'évaluation de cette expression?
```
-(3 + 4) - 4 // 2 + 2 * (4) - (-3 + 1)
```
```
Trace: (en appliquant la priorité des opérateurs PEDMAS)
-(3 + 4) - 4 // 2 + 2 * (4) - (-3 + 1)
-(3 + 4) - 2 + 8 - (-3 + 1)
-(7) - 2 + 8 - (-2)
-7 - 2 + 8 + 2
1

Réponse:
L'entier qu'on obtiendra à la suite de l'évaluation de l'expression est 1.
```
### Solutionnaire
```
1
Parenthèses d'abord: -7 - 4 // 2 + 2 * 4 - -2
Multiplication et division: -7 - 2 + 8 - -2
Addition et soustraction: 1
```
## Question 11
Quel booléen obtiendra-t-on suite à l'évaluation de cette expression?
```
(Vrai et Faux) ou Vrai
```
```
Trace: (en appliquant la priorité des opérateurs PEDMAS)
(Vrai et Faux) ou Vrai
(Faux) ou Vrai
Faux ou Vrai
Vrai

Réponse:
Le booléen qu'on obtiendra à la suite de l'évaluation de l'expression est Vrai.
```
### Solutionnaire
```
Vrai

Vrai et faux devient Faux, puis Faux ou Vrai devient Vrai
```
## Question 12
Quel booléen obtiendra-t-on suite à l'évaluation de cette expression contenant des entiers?
```
(3 > 2) et (4 + 5 * 2 == 18)
```
```
Trace: (en appliquant la priorité des opérateurs PEDMAS)
(3 > 2) et (4 + 5 * 2 == 18)
(3 > 2) et (4 + 10 == 18)
(3 > 2) et (14 == 18)
(Vrai) et (Faux)
Vrai et Faux
Faux

Réponse:
Le booléen qu'on obtiendra à la suite de l'évaluation de l'expression est Faux.
```
### Solutionnaire
```
Faux
3 > 2 est vrai, mais 4 + 5 * 2 donne 14, non pas 18. L'expression booléenne évaluée est donc Vrai et Faux, ce qui donne Faux.
```
## Question 13
Quel réel obtiendra-t-on suite à l'évaluation de cette expression?
```
3.5 * 2 + 8 // 3 + 7.0 / (-1 - 1.0)
```
```
Trace: (en appliquant la priorité des opérateurs PEDMAS)
3.5 * 2 + 8 // 3 + 7.0 / (-1 - 1.0)
3.5 * 2 + 8 // 3 + 7.0 / (0.0) # Explication de l'erreur sur le résultat de l'expression (-1 - 1.0) : Le résultat est -2.0 et non 0.0.
7 + 2 + ERROR
ERROR

Réponse:
On ontiendra pas de réel,  
voir même aucune donnée, 
à la suite de l'évaluation de l'expression.
La division par zéro génère une erreur.

{
Division by zero raises the ZeroDivisionError exception.
}
Article: 6.7. Binary arithmetic operations
Source: https://docs.python.org/3/reference/expressions.html#binary-arithmetic-operations
```
### Solutionnaire
```
5.5
Parenthèses d'abord: 3.5 * 2 + 8 // 3 + 7.0 / -2.0
Multiplication et division: 7.0 + 2 - 3.5
Addition et soustraction: 5.5
Attention! L'opération a // b est une division entière. Elle indique combien de fois b entre entièrement dans a.
L'opération a / b est quant à elle la division classique qui peut donner des nombres à virgule.
```
## Question 14
Quel booléen obtiendra-t-on suite à l'évaluation de cette expression?
```
neg (Faux ou Faux) ou neg (Vrai et Vrai)
```
```
Trace: (en appliquant la priorité des opérateurs PEDMAS)
neg (Faux ou Faux) ou neg (Vrai et Vrai)
neg (Faux) ou neg (Vrai)
Vrai ou Faux
Vrai

Réponse:
Le booléen qu'on obtiendra à la suite de l'évaluation de l'expression est Vrai.
```
### Solutionnaire
```
Vrai
(Faux ou Faux) devient Faux, alors que (Vrai et Vrai) devient Vrai. On obtient alors neg Faux ou neg Vrai, ce qui devient Vrai ou Faux, ce qui donne Vrai.
```
## Question 15
Quel booléen obtiendra-t-on suite à l'évaluation de cette expression contenant des entiers?
```
neg (3 > 2 et Vrai) ou 4 == 12 // 4
```
```
Trace: (en appliquant la priorité des opérateurs PEDMAS)
neg (3 > 2 et Vrai) ou 4 == 12 // 4
neg (Vrai et Vrai) ou 4 == 3
neg Vrai ou Faux
Faux ou Faux
Faux  

Réponse:
Le booléen qu'on obtiendra à la suite de l'évaluation de l'expression contenant des entiers est Faux.
```
### Solutionnaire
```
Faux
Parenthèses d'abord: (3 > 2 et Vrai) devient (Vrai et Vrai) qui devient Vrai.
Opérateurs arithmétiques: 12 // 4 donne 3.
Opérateurs de comparaison: 4 == 3 donne faux.
Il reste neg Vrai ou Faux, qui devient Faux ou Faux, qui devient Faux.
```
## Question 16
Remplissez ce programme trouvant le maximum entre deux nombres en remplaçant la ligne # par votre code (utiliser l'instruction si!):
```
nombre_1 <- Demander("Un premier nombre:")
nombre_2 <- Demander("Un deuxième nombre:")
#
Afficher("Le plus grand nombre est:", plus_grand_nombre)
```
```
nombre_1 <- Demander("Un premier nombre:")
nombre_2 <- Demander("Un deuxième nombre:")
Si nombre_1 > nombre_2 alors:
    plus_grand_nombre <- nombre_1
Sinon:
    plus_grand_nombre <- nombre_2
Afficher("Le plus grand nombre est:", plus_grand_nombre)
```
### Solutionnaire
```
nombre_1 <- Demander("Un premier nombre:")
nombre_2 <- Demander("Un deuxième nombre:")
si nombre_1 > nombre_2 alors:
    plus_grand_nombre <- nombre_1
sinon:
    plus_grand_nombre <- nombre_2
Afficher("Le plus grand nombre est:", plus_grand_nombre)
```
## Question 17
Quel entier donné en entrée résulterait en l'affichage du "Bravo!" ?
```
x <- Demander("Tentez de deviner l'entier secret:")
si neg (x <= 10 ou x >= 15) alors:
    si x % 3 == 1 alors:
        Afficher("Bravo!")
    fin si
fin si
```
```
1: x <- Demander("Tentez de deviner l'entier secret:")
2: si neg (x <= 10 ou x >= 15) alors:
3:     si x % 3 == 1 alors:
4:         Afficher("Bravo!")
5:     fin si
6: fin si

Trace:
x
10
si neg (10 <= 10 ou 10 >= 15)
si neg (Vrai ou Faux)
si neg Vrai
Faux
fin si

x
15
si neg (15 <= 10 ou 15 >= 15)
si neg (Faux ou Vrai)
si neg Vrai
Faux
fin si

# La variable x doit être entre 11 et 14 inclusivement.

x
13
si neg (13 <= 10 ou 13 >= 15)
si neg (Faux ou Faux)
si neg Faux
si Vrai alors:
si 13 % 3 == 1
13 % 3 # 4 reste 1
1
si 1 == 1
si Vrai alors:
Bravo!
fin si
fin si

Réponse:
L'entier donné en entrée qui résulterait en l'affichage du "Bravo!" est 13.
```
### Solutionnaire
```
13
Il s'agit du seul entier entre 11 et 14 inclusivement qui est un multiple de 3 additionné de 1.
```
## Question 18
Quel entier donné en entrée résulterait en l'affichage du "Bravo!" ?
```
x <- Demander("Tentez de deviner l'entier secret:")
y <- x * 2
si x % 3 == 0 alors:
    y <- y * 2
fin si
si x > 5 et y < 15 alors:
    Afficher("Bravo!")
fin si
```
```
1: x <- Demander("Tentez de deviner l'entier secret:")
2: y <- x * 2
3: si x % 3 == 0 alors:
4:     y <- y * 2
5: fin si
6: si x > 5 et y < 15 alors:
7:     Afficher("Bravo!")
8: fin si

Analyse:
#si x % 3 == 0 # x ne doit pas être un multiple de 3,
#y <- y * 2 # sinon y est agrandit, 
#si x > 5 et y < 15 # et ne pourra pas peut être pas être plus petit que 15. (exclure 6, 9, 12, 15, ...)

Trace:
x
7
y
14
si x % 3 == 0
si 7 % 3 == 0
si 1 == 0
si faux
fin si
si x > 5 et y < 15
si 7 > 5 et 14 < 15
si Vrai et Vrai
si Vrai alors:
Bravo!
fin si

Réponse:
L'entier donné en entrée qui résulterait en l'affichage du "Bravo!" est 7.
```
### Solutionnaire
```
7
Il faut malheureusement y aller à tâtons en faisant la trace pour plusieurs entiers!
Avec 7 vous avez y = 14 et comme 7 n'est pas divisible par 3 y n'est pas augmenté davantage.
Avec 6 vous auriez y = 12, puis y = 24 car 6 est divisible par 3.
Avec 8 vous auriez y = 16, ce qui est d'emblée trop grand.
```
## Question 19
Donnez l'affichage de l'algorithme suivant:
```
x <- 0
si x >= 12 alors:
    si x == 0 alors:
        x <- 12
    sinon:
        x <- 24
    fin si
sinon:
    si x <= 12 alors:
        x <- 36
    sinon:
        x <- 48
    fin si
fin si
Afficher(x // 12)
```
```
 1: x <- 0
 2: si x >= 12 alors:
 3: 
 4:      si x == 0 alors:
 5:         x <- 12
 6:     sinon:
 7:         x <- 24
 8:     fin si
 9: sinon:
10:     si x <= 12 alors:
11:         x <- 36
12:     sinon:
13:         x <- 48
14:     fin si
15: fin si
16: 
17: Afficher(x // 12)

Trace:
x
0
si 0 >= 12
si Faux
sinon:
si x <= 12
si Vrai alors:
x
36
fin si
x // 12
36 // 12
3

Réponse:
L'algorithme affiche ce qui suit:
3
```
### Solutionnaire
```
3
Comme x vaut d'abord 0, il est plus petit que 12, donc on va directement à la deuxième partie, le bloc sinon.
x vaut toujours 0, ce qui est plus petit ou égal à 12, alors x prend la valeur 36. Ensuite on affiche 36 // 12, c'est-à-dire 3.
```
## Question 20
Donnez l'affichage de l'algorithme suivant:
```
x <- 0
somme <- 0
tant que x <= 10 faire:
    somme <- somme + x
    x <- x + 1
fin tant que
Afficher(somme)
```
```
1: x <- 0
2: somme <- 0
3: tant que x <= 10 faire:
4:     somme <- somme + x
5:     x <- x + 1
6: fin tant que
7: Afficher(somme)

Trace:
x
0
somme
0
tanque x <= 10 faire: # Lorsque la variable x est égale a 11, fin tant que
somme
somme + x
0 + 0, 0 + 1, 1 + 2, 3 + 3, 6 + 4, 10 + 5, 15 + 6, 21 + 7, 28 + 8, 36 + 9, 45 + 10 
somme
0, 1, 3, 6, 10, 15, 21, 28, 36, 45, 55
x
x + 1
0 + 1, 1 + 1, 2 + 1, 3 + 1, 4 + 1, 5 + 1, 6 + 1, 7 + 1, 8 + 1, 9 + 1, 10 + 1
x
1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11

Réponse:
L'algorithme affiche ce qui suit:
55
```
### Solutionnaire
```
55

Note: Cet algorithme calcule la somme de 10, 9, 8, ..., 1, 0, ce qui donne 55.
```
## Question 21
À l'aide d'une boucle tant que, écrivez un algorithme qui calcule la somme de tous les nombres plus petits ou égaux à un nombre fourni en entrée en remplaçant la ligne # par votre code.
```
# Précision apporté à la question:
# [...] qui calcule la somme de tous les nombres [entiers et positifs] plus petits ou égaux à un nombre [entier et positif] fourni en entrée [...]

x <- Demander("Entier fourni:")
#
Afficher(somme)
```
```
x <- Demander("Entier fourni:")
somme <- 0
tant que x > 0 faire:
    somme <- somme + x
    x <- x + 1 # Explication de l'erreur de l'opération arithmétique effectué sur la variable x qui agit en tant qu'itérateur : Il faut faire x - 1 au lieu de x + 1 puisque la bouble part de x à 0, l'itérateur doit être décrémenté et non incrémenté. 
fin tant que
Afficher(somme)

# L'erreur aurait pu être décelé en faisant la trace.
Trace:
x
3
tant que x > 0
tant que 3 > 0
tant que Vrai
somme
somme + x
0 + 3
x = x + 1
3 + 1
4 # Oupsss! 4 est plus grand que le nombre entier fourni.
```
### Solutionnaire
```
x <- Demander("Entier fourni:")
i <- 0
somme <- 0
tant que i <= x faire:
    somme <- somme + i
    i <- i + 1
fin tant que
Afficher(somme)
ou

x <- Demander("Entier fourni:")
somme <- 0
tant que x > 0 faire:
    somme <- somme + x
    x <- x - 1
fin tant que
Afficher(somme)
```
## Question 22
Réécrivez votre algorithme de la question précédente avec une boucle pour tout.
```
x <- Demander("Entier fourni:")
somme <- 0
pour tout i dans (1, 2, ..., x) faire: # Explication de l'erreur de la représentation de la séquence en pseudo-code : Il faut utilisé <, signe inférieur à, au lieu de la paranthèse gauche; et >, signe supérieur à, au  lien de la paranthèse droite.
    somme <- somme + i
    i <- i + 1
fin pour tout
Afficher(somme)

# Je n'ai pas jugé nécessaire de débuter la séquence à 0 puisque cette valeur n'affecte pas la somme.
```
### Solutionnaire
```
x <- Demander("Entier fourni:")
somme <- 0
pour tout i dans <0,1,...,x> faire:
    somme <- somme + i
fin pour tout
Afficher(somme)
```