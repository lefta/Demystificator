# Les Vecteurs - Qu'est ce qu'un vecteur

## A quoi ça ressemble

Ça ressemble à une collection de trois ou quatre nombres:

    [2, 6, 8, 1]

Plus tard dans ce cours, nous utiliserons ce vecteur générique:

    [x, y, z, w]

### X

C'est la valeur horizontale du vecteur.

### Y

C'est la valeur verticale du vecteur.

### Z

C'est la valeur de profondeur du vecteur. Elle peut être omise sur un plan 2D.

### W

Cette valeur est un peu spéciale:
* Si elle est égale à 0, le vecteur représente une direction
* Si elle a une quelconque autre valeur, il s'agit d'un multiplicateur à appliquer aux autres
    valeurs et le vecteur représente un point

Si le but n'est que de stocker des valeurs, elle peut être omise. Si le but est de manipuler le
vecteur par la suite (avec des matrices par exemple), elle est requise.

## A quoi ça sert

À stocker et manipuler des coordonées de point ou des directions.
