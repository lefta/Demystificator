# Les matrices - La matrice de vue

## Données d'entrée

La matrice de vue peut être configurée à l'aide de trois vecteurs. Les noms entre parenthèses seront
ceux utilisés dans les calculs.

* l'oeil (eye): la position de la caméra
* la cible (target): le point que la caméra va regarder
* le sens (up): la direction du haut de la caméra

## La matrice en elle même

Nous allons définir 3 vecteurs intermédiaires pour nous faciliter la tache:

    f = normal(target - eye)
    s = normal(cross(f, up))
    u = cross(s, f)

Puis, la matrice:

| | | | |
|---|---|---|---|
| sx | sy | sz | -dot(s, eye) |
| ux | uy | uz | -dot(u, eye) |
| -fx | -fy | -fz | dot(f, eye) |
| 0 | 0 | 0 | 1 |
