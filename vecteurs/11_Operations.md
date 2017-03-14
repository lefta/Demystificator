# Les vecteurs - Les opérations

## Nomenclature

* Les suffixes `1` et `2` désignent les valeurs du premier et du deuxième vecteur, respectivement
* Le suffixe `r` désigne les valeurs du vecteur résultant de l'opération

Les noms entre parenthèses peuvent être réutilisés par d'autres calculs et / ou cours.

Les valeurs non utilisées peuvent être omises des calculs.

## La soustraction

    xr = x1 - x2;
    yr = y1 - y2;
    zr = z1 - z2;
    wr = w1 - w2;

## La longueur (len)

    sqrt(x.x + y.y + z.z)

## La normalisation (normal)

    rx = x1 / len(v1)
    ry = y1 / len(v1)
    rz = z1 / len(v1)
    rw = w1 / len(v1)

## Produit vectoriel (cross)

Ce calcul n'est applicable qu'aux vecteurs 3D (à trois ou quatre composantes)

    rx = y1.z2 - z1.y2
    ry = z1.x2 - x1.z2
    rz = x1.y2 - y1.x2

## Produit scalaire (dot)

    x1.x2 + y1.y2 + z1.z2
