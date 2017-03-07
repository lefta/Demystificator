# Les matrices - La matrice de projection

Cette page ne présentera que la matrice de projection en perspective. Il ne doit pas être si
compliqué de trouver la matrice de projection orthogonale.

## Notions nécessaires

La matrice de projection va utiliser quelques notions que vous ne possédez pas forcément:

### FOV: le champs de vue

Le champ de vue va définir la quantité de ce que vous voyez. Plus il sera élevé, plus vous verrez de
choses mais plus elles vous paraitront éloignées, plus il sera petit et moins vous verrez de choses
et paraitrez proches des objets. Trouvez le FOV qui vous convient, placez le en constante dans votre
programme et n'y touchez plus. Une valeur de 45 degrés peut être un bon début.

### Aspect ratio

L'aspect ratio est la largeur de votre écran. Il sera abrégé `ar` par la suite. Vous savez surement
ce que c'est, vous ne connaissez juste pas son nom. Si vous avez entendu parler d'écrans 4/3, 19/9,
etc, vous voyez. Sinon, c'est la largeur de votre écran divisé par sa hauteur.

### Bounding box

La bounding box (désolé, encore un nom anglais) est la boite contenant la partie visible de votre
scène. Elle est composée de deux constantes:
* zNear: La partie proche de la bounding box. C'est la distance avant que les objets soient
affichés. Plus cette valeur est petite, mieux c'est.
* zFar: La partie lointaine de la bounding box. C'est la distance sur laquelle vos objets seront
affichés. Plus elle est grande, mieux c'est.

Ces deux valeurs doivent rester positives. Comme pour le FOV, trouvez celles qui vous conviennent et
n'y touchez plus. 0.1 pour zNear et 100 pour zFar peuvent être de bonnes valeurs pour démarrer.

## La matrice en elle même

Attention: La valeur du FOV doit être convertie en radians!

D'abord, nous avons besoin d'un petit calcul pour nous faciliter la tache: `thfov = tan(fov/2)`.

Puis, la matrice:

| | | | |
|---|---|---|---|
| 1/(ar.thfov) | 0 | 0 | 0 |
| 0 | 1/thfov | 0 | 0 |
| 0 | 0 | zFar/(zNear-zFar) | -1 |
| 0 | 0 | -(zFar.zNear)/(zFar-zNear) | 1 |

