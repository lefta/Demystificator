# Les matrices - Qu'est ce qu'une matrice

## A quoi ça ressemble

Ça ressemble à un tableau en deux dimensions tout ce qu'il y a de plus standard (les nombres sont
choisis au hasard) :

| | | | |
|---|---|---|---|
| 1 | 13 | 0.5 | 12 |
| 5 | 0.01 | 4.7 | 34 |
| 5 | 9.8 | 0 | -1 |
| 4 | -1.3 | 90 | 33.3 |

Plus tard dans ce cours, nous utiliserons cette matrice théorique :

| | | | |
|---|---|---|---|
| a | b | c | d |
| e | f | g | h |
| i | j | k | l |
| m | n | o | p |

Les matrices peuvent exister de toutes tailles, mais nous n'aurons besoin que de matrices de 4x4.


## A quoi ça sert

En théorie, une matrice sert à appliquer une série d'opération à la chaine à une série de données.

En pratique, avec les bonnes matrices, celà permettra d'appliquer automatiquement des
transformations à nos objets. Chaque point de notre objet sera multiplié par la matrice de façon à
déplacer, tourner, etc notre objet.
