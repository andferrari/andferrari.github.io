---
layout: course
title: Inverse problems
description: Learn how to numerically solve an inverse problem to reconstruct an image
instructor: 
year: 2026
term: 
location: 
time: 
course_id: IP ESTEL2
---
## Description

L'objectif de ce cours est de présenter une approche unifiée pour la résolution des problèmes inverses en imagerie.


![s](/assets/img/teaching/Problemes-Inverses-t.png)

## Programme

1. Introduction aux problèmes inverses
   - Exemples : tomographie (rayons X), imagerie RADAR, imagerie optique
   - Modèle direct : cas général
   - Modèle direct linéaire, cas spatialement invariant

2. Rappels de traitement numérique du signal et des images
   - Systèmes linéaires et invariants, réponse impulsionnelle, convolution
   - Transformée de Fourier, transformée de Fourier discrète (TFD)
   - Convolution circulaire
   - Transformée de Fourier rapide (FFT)
   - Extension aux images : linéarité, invariance spatiale, stabilité
   - Convolution et transformée de Fourier des images
   - Égalisation d'histogramme

3. Résolution d'un problème inverse : formalisation
   - Définition et propriétés d'un problème linéaire
   - Résolution « naïve » par filtrage inverse et amplification du bruit
   - Inversion par moindres carrés : cas général et cas d'une convolution
   - Régularisation : introduction d'un a priori
   - Exemples d'a priori en 1D et en 2D, régularisation de Tikhonov

4. Introduction à l'optimisation convexe
   - Formulation d'un problème d'optimisation, programmation linéaire
   - Ensembles et fonctions convexes, fonctions quadratiques
   - Problème d'optimisation convexe et caractérisation de la solution
   - Algorithmes de descente
   - Choix du pas : pas exact, dichotomie, backtracking d'Armijo
   - Descente de gradient et vitesse de convergence
   - Descente de Newton, algorithmes quasi-Newton, vitesse de convergence
   - Dualité et conditions de Karush-Kuhn-Tucker
   - Gradient projeté
   - Optimisation sous contraintes d'égalité et d'inégalité
   - Barrière logarithmique et algorithme du point intérieur

5. Résolution d'un problème inverse : modèle direct convolutif
   - Calcul de l'erreur de reconstruction
   - Choix du paramètre de régularisation
   - Déconvolution par filtrage inverse
   - Calcul du gradient et de l'opérateur adjoint (convolution linéaire et circulaire)
   - Exemples de régularisations : Tikhonov, lissage, Tikhonov généralisé, positivité, préservation des bords
   - Régularisation quadratique et calcul de la solution en fréquence


## Travaux pratiques

Une large part du cours est consacrée à des projets pratiques, au cours desquels les étudiants implémenteront différents algorithmes et confronteront les résultats théoriques aux résultats de simulation. Les calculs seront réalisés de préférence en Julia ou en Python.

   - TP 1 : bases du traitement d'image (format, codage, colormap, échantillonnage spatial, fréquences spatiales, convolution, détection de contours)
   - TP 2 : convolution linéaire et convolution circulaire d'images
   - TP 3 : descente de gradient (pas fixe, pas optimal, backtracking) et descente de Newton
   - TP 4 : filtre de Wiener, inversion par minimisation d'une fonction de coût, réglage du paramètre de régularisation, contrainte de positivité
       
## Évaluation

- Contrôles courts (4) : 40 %
- Examen final : 30 %
- Projet : 30 %
