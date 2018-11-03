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

## Le produit mixte (comb)

Le produit mixte est parfois aussi appelé (abusivement) produit vectoriel. Si vous entendez parler
de produit vectoriel sur un veteur 2D, il s'agit d'un produit mixte.

Ce calcul n'est applicable qu'aux vecteurs 2D

    x1 * y2 - x2 * y1

## La longueur (len)

    sqrt(x.x + y.y + z.z)

## La normalisation (normal)

    xr = x1 / len(v1)
    yr = y1 / len(v1)
    zr = z1 / len(v1)
    wr = w1 / len(v1)

## Produit vectoriel (cross)

Ce calcul n'est applicable qu'aux vecteurs 3D (à trois ou quatre composantes)

    xr = y1.z2 - z1.y2
    yr = z1.x2 - x1.z2
    zr = x1.y2 - y1.x2

## Produit scalaire (dot)

    x1.x2 + y1.y2 + z1.z2
