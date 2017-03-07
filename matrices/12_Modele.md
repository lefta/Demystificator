# Les matrices - La matrice de modèle

La matrice de modèle est une combinaison des matrices de transformation d'un modèle, décrites ci
dessous.


## La matrice de déplacement

La matrice de déplacement sert à déplacer notre objet selon les axes X, Y et Z. La valeur est
dépendante de l'espace de référence. Par exemple, 1 déplace l'objet d'une unité (quelle que soit
votre unité) dans le sens de l'axe. \>0 déplace dans le sens de l'axe (pour X, vers la droite),
\<0 déplace dans le sens inverse de l'axe (pour X, vers la gauche).

| | | | |
|---|---|---|---|
| 1 | 0 | 0 | x |
| 0 | 1 | 0 | y |
| 0 | 0 | 1 | z |
| 0 | 0 | 0 | 1 |

## La matrice d'échelle

La matrice d'échelle sert à redimensionner notre objet selon les axes X, Y et Z. 1 correspond à la
taille originelle, \<1 réduit la taille de l'objet et \>1 agrandit la taille de l'objet. De façon
générale, votre échelle sera de `x% / 100`. Par exemple, pour diviser par deux votre taille (soit
une échelle de 50%), vous mettrez la valeur `50 / 100 = 0.5`.

| | | | |
|---|---|---|---|
| x | 0 | 0 | 0 |
| 0 | y | 0 | 0 |
| 0 | 0 | z | 0 |
| 0 | 0 | 0 | 1 |

## La matrice de rotation

Les matrices de rotation servent à faire tourner votre objet sur l'axe correspondant à la matrice
selon un angle `a`.

Attention!

* Étant donné que les valeurs des matrices de rotation s'écrasent les unes les autres, elles sont
définies séparément pour chacun des axes. Vous pourrez vous amuser à définir une matrice unique
quand vous saurez les combiner.
* Ces matrices font tourner l'objet selon l'axe, ce qui peut paraitre contre intuitif: une rotation
selon l'axe Y fera tourner votre objet de gauche à droite et vice versa.
* Pour chacune de ces trois matrices, l'angle de rotation est exprimé en radians. Assurez vous
d'avoir fait la conversion.

### Rotation selon l'axe X

| | | | |
|---|---|---|---|
| 1 | 0 | 0 | 0 |
| 0 | cos(a) | -sin(a) | 0 |
| 0 | sin(a) | cos(a) | 0 |
| 0 | 0 | 0 | 1 |

### Rotation selon l'axe Y

| | | | |
|---|---|---|---|
| cos(a) | 0 | sin(a) | 0 |
| 0 | 1 | 0 | 0 |
| -sin(a) | 0 | cos(a) | 0 |
| 0 | 0 | 0 | 1 |

### Rotation selon l'axe Z

| | | | |
|---|---|---|---|
| cos(a) | -sin(a) | 0 | 0 |
| sin(a) | cos(a) | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 0 | 0 | 1 |
