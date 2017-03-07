# Les matrices - La matrice MVP

Pour commencer, derrière ce nom barbare est l'acronyme de Modèle - Vue - Projection. C'est la
matrice qui nous permettra de faire notre rendu exactement comme on le veut.

## Modèle

C'est la matrice qui transformera notre modèle. C'est la plus simple à comprendre, elle permet de
placer le modèle où l'on veut dans le rendu de notre monde.

Quand vous dessinez une armée, vous pouvez avoir un modèle par membre de votre armée, ou n'avoir
qu'un seul modèle que l'on déplace et redessine autant de fois que l'on veut. C'est l'utilité de la
matrice de modèle; c'est très pratique et la mémoire de votre ordinateur vous en remerciera.


## Vue

La matrice de vue correspond à notre caméra. Elle nous permet de déplacer les objets pour les faire
entrer (ou non) dans le rendu dessiné à l'écran.

Pour changer de plan quand vous filmez une montagne, vous pouvez déplacer soit la caméra, soit la
montagne. Déplacer la montagne est compliqué dans la vraie vie, mais très facile en programmation
3D: c'est juste une matrice.


## Projection

C'est la matrice qui va transformer vos objets de façon à rendre le rendu réaliste. Concrétement,
elle ajoute l'effet de profondeur (ce qui est plus loin est plus petit) et peut servir à corriger
l'aspect de votre rendu pour l'adapter au format l'écran.


## La matrice d'identité

La matrice d'identité est un peu spéciale: elle ne fait rien (d'où son nom). Elle conservera nos
points tels quels, c'est pourquoi elle est présentée ici, elle ne rentre dans aucune des catégories
précitées.

| | | | |
|---|---|---|---|
| 1 | 0 | 0 | 0 |
| 0 | 1 | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 0 | 0 | 1 |
