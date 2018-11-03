# Recette - Rotation en drag n' drop

## Préambule

Cette recette vous permettra de faire une rotation en drag n' drop, autrement dit, de permettre à
l'utilisateur de faire tourner un objet avec sa souris sur un plan 2D.

### Prérequis

* Savoir ce qu'est un vecteur en programmation 2D
* Savoir utiliser la fonction arc-cosinus (acos)
* Savoir ce qu'est un radian
* Connaitre le théorème de pythagore

### Données de base

* le point o, qui est l'origine de votre rotation
* le point s, qui est le point de départ de la rotation (là où l'utilisateur a cliqué)
* le point e, qui est le point d'arrivée de la rotation (là où la souris est actuellement)


## La recette

### Les cotés du triangle

Pour commencer, vous avez besoin de la longueur des cotés de votre triangle. Celà se trouve
facilement avec pythagore, et c'est une notion apprise en 4eme, vous ne devriez pas avoir de
problème avec.

Dans la suite de cette recette, ces cotés seront appelés `os`, `oe` et `se`.

### Calcul de l'angle

Nous utilisons pour cela la loi des cosinus.

	acos((se * se * -1 + os * os + oe * oe) / (2 * os * oe))

### Le signe de l'angle

Si vous avez déja testé le calcul ci dessus, vous aurez remarqué que cet angle est toujours positif.
Il nous faut donc son signe pour effectuer une rotation dans le sens contraire des aiguilles d'une
montre.

Soient les vecteurs :

* a: o->s ({ xs - xo, ys - yo })
* b: o->e ({ xe - xo, ye - yo })

Le signe de votre angle sera simplement le signe de :

	comb(a, b)

## L'auteur

Cédric Legrand, a.k.a. Lefta.

Développeur freelance et programmeur par passion, titulaire d'un bac pro ébénisterie, j'ai étudié à
l'école 42 à Paris.

Passionné par le bas niveau (C/C++), le système (Linux) et le graphisme (OpenGL), mais curieux et
touche à tout.
