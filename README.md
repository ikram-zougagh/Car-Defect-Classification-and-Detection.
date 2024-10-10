# Projet de Classification et Détection des Défauts de Voitures

## Description du projet
Ce projet vise à classifier les voitures endommagées et non endommagées à l'aide de deux modèles de réseaux de neurones : CNN et VGG19. Après la classification, nous avons utilisé Detectron2 pour la détection des défauts sur une base de données différente.

## Objectifs :
- Comparer la performance de **CNN** et **VGG19** pour la classification binaire.
- Utiliser **Detectron2** pour la détection des défauts sur des images de voitures.

## Modèles de Classification
Nous avons formé deux modèles différents pour la classification binaire des voitures en deux catégories : endommagées et non endommagées. Voici les détails :

### Modèle CNN :
Nous avons construit un modèle de réseau neuronal convolutif (**CNN**) personnalisé, entraîné sur un jeu de données d'images de voitures endommagées et non endommagées. Le CNN a montré des résultats impressionnants avec une précision de **91,46%** sur le jeu de validation. Ce modèle a bien généralisé sur des données non vues pendant l'entraînement, ce qui en fait un choix solide pour cette tâche de classification.

#### Résultats de CNN :
- **Précision de validation** : 91,46%
- **Perte de validation** : Faible perte, indiquant une bonne généralisation.
- **Mesures d'évaluation** : Précision, rappel, et F1-score ont été calculés et montrent une bonne performance dans la classification des deux classes.

### Modèle VGG19 :
Nous avons également testé le modèle **VGG19**, une architecture pré-entraînée, afin de comparer ses performances avec le CNN. VGG19 a montré une précision légèrement inférieure, avec des signes de surapprentissage (**overfitting**) indiqués par une fluctuation notable dans les résultats de validation.

#### Résultats de VGG19 :
- **Précision de validation** : 50%
- **Problèmes rencontrés** : Surapprentissage observé, ce qui a conduit à une performance inférieure comparée au CNN.
- **Mesures d'évaluation** : Précision, rappel et F1-score étaient significativement plus bas que ceux du CNN.

## Comparaison des Modèles :
Le **CNN** a surpassé **VGG19** en termes de généralisation et de précision, ce qui fait de lui le meilleur modèle pour la classification binaire des voitures endommagées et non endommagées dans notre cas.

## Détection des Défauts avec Detectron2
Après la classification, nous avons utilisé **Detectron2**, un framework de détection d'objets développé par **Meta** (anciennement Facebook AI), pour la détection des défauts dans les voitures. Nous avons utilisé une base de données différente spécialement conçue pour la détection de défauts visuels.

### Étapes :
- **Prétraitement des données** : Nous avons préparé un autre jeu de données pour la détection avec Detectron2.
- **Entraînement** : Nous avons formé un modèle de détection basé sur une architecture de type **Faster R-CNN** disponible dans Detectron2.
- **Résultats** : Le modèle a détecté efficacement plusieurs types de défauts visuels sur les images de test.

## Base de Données
- **Classification binaire** : Un jeu de données contenant des images de voitures endommagées et non endommagées a été utilisé pour entraîner les modèles CNN et VGG19.
- **Détection des défauts** : Un second jeu de données, distinct, a été utilisé pour la tâche de détection avec Detectron2.

## Conclusion
En conclusion, l'analyse des résultats a montré que le **CNN** était plus performant que **VGG19** pour la classification binaire des voitures. Ensuite, **Detectron2** s'est avéré efficace pour la détection des défauts, ouvrant la voie à une intégration dans des systèmes de détection de défauts automatiques pour l'industrie automobile.
