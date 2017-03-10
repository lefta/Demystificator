# Les matrices - Combinaison

## Fuuuusionnnn

Pour fusionner des matrices, il suffit de les multiplier entre elles.

Nomenclature:
* Nomenclature définie dans le chapitre 1-0
* l: ligne en cours de multiplication. Si on calcule la valeur en [3;2], l sera 3.
* c: colonne en cours de multiplication. Si on calcule la valeur en [3;2], c sera 2.
* suffixes 1 et 2: donnée de la première et deuxième matrice, respectivement.

La méthode générale est simple, il suffit de multiplier la ligne courante par la colonne courante.
Ehm, pour le coup, un calcul vaut mieux qu'un long discours. Pour calculer le résultat en [l;c]:
`l1[0].c2[0]+l1[1].c2[1]+...`, où ... continue jusqu'à la dimension de la matrice.

Je vous mache le travail, voici notre matrice multipliée:

| | | | |
|---|---|---|---|
| a1.a2+b1.e2+c1.i2+d1.m2 | a1.b2+b1.b2+c1.j2+d1.n2 | a1.c2+b1.g2+c1.k2+d1.o2 | a1.d2+b1.h2+c1.l2+d1.p2 |
| e1.a2+f1.e2+g1.i2+h1.m2 | e1.b2+f1.f2+g1.j2+h1.n2 | e1.c2+f1.g2+g1.k2+h1.o2 | e1.d2+f1.h2+g1.l2+h1.p2 |
| i1.a2+j1.e2+k1.i2+l1.m2 | i1.b2+j1.f2+k1.j2+l1.n2 | i1.c2+j1.g2+k1.k2+l1.o2 | i1.d2+j1.h2+k1.l2+l1.p2 |
| m1.a2+n1.e2+o1.i2+p1.m2 | m1.b2+n1.f2+o1.j2+p1.n2 | m1.c2+n1.g2+o1.k2+p1.o2 | m1.d2+n1.h2+o1.l2+p1.p2 |


## L'ordre compte

Faites attention à l'ordre dans lequel vous multipliez vos matrices, si vous les multipliez dans un
ordre différent, vous obtiendrez un résultat différent.

Pour vous faire une idée, on va faire une expérience:
* Avancez d'un pas (attention à votre ordi) puis tournez à gauche
* Tournez à gauche puis avancez d'un pas

Vous vozez la différence?


## Construire la matrice de modèle

La matrice de modèle est composée de cinq matrices présentées dans le chapitre dédié. En réalité,
l'ordre va dépendre du résultat attendu. Si vous déplacez en premier, l'origine de la rotation
changera et l'objet ne tournera plus sur lui même. En revanche, si vous tournez en premier, l'axe de
l'objet changera et il ne se déplacera plus dans la même direction.


## Construire la matrice MVP finale

Encore une fois, l'ordre importe. Le bon ordre pour construire la matrice est
`projection.vue.modèle`.
