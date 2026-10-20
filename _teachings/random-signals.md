---
layout: course
title: Random signals
description: Analyser et filtrer les signaux aléatoires
instructor: André Ferrari
year: 2026
term: 
location: 
time: 
term: 
course_id: 
---

Ce cours est destiné aux étudiants du Master 1  [ESTEL](https://univ-cotedazur.fr/formation/offre-de-formation/master-electronique-energie-electrique-automatique). 

![s](/assets/img/teaching/sinus.png){: width="400"}

## Programme


1. Introduction : exemples de signaux aléatoires
   - Générateur sinusoïdal à phase initiale aléatoire
   - Signal mesuré en présence de bruit
   - Émetteur de symboles binaires

2. Rappels de probabilités
   - Espace de probabilité, événements, probabilité conditionnelle, indépendance
   - Variable aléatoire : fonction de répartition, densité de probabilité, cas discret et continu
   - Moyenne, variance, écart type
   - Loi gaussienne
   - Couples de variables aléatoires : loi conjointe, lois marginales et conditionnelles, indépendance
   - Covariance, coefficient de corrélation, décorrélation et indépendance
   - Cas de N variables aléatoires : vecteur moyenne, matrice de covariance
   - Vecteurs gaussiens : marginales, décorrélation et indépendance, transformation affine

3. Signaux aléatoires
   - Définition d'un signal aléatoire
   - Stationnarité au sens strict et au sens large
   - Moments d'ordre 1 et 2 : moyenne, autocorrélation, autocovariance
   - Exemple : sinusoïde à phase aléatoire, puissance
   - Matrice de covariance, propriétés (symétrique, définie positive)
   - Intercorrélation et intercovariance de deux signaux
   - Bruit i.i.d. et bruit blanc
   - Exemples de signaux stationnaires et non stationnaires
   - Matrice de covariance de Toeplitz
   - Sortie d'un filtre RIF excité par un bruit blanc

4. Analyse spectrale des signaux aléatoires
   - Rappel : densité spectrale d'énergie d'un signal déterministe, Parseval
   - Densité spectrale de puissance d'un signal stationnaire
   - Théorème de Wiener-Khintchine, en temps discret et en temps continu
   - Exemple : densité spectrale d'un bruit i.i.d.
   - Exercices : processus à moyenne mobile, marche aléatoire, processus autorégressif d'ordre 1
   - Bruit blanc en temps continu

5. Filtrage des signaux aléatoires
   - Rappels sur le filtrage linéaire invariant, cas déterministe
   - Moyenne et autocorrélation de la sortie d'un filtre
   - Intercorrélation entrée-sortie
   - Théorème des interférences

6. Processus de Poisson et signal télégraphique
   - Rappels sur la loi de Poisson
   - Processus de Poisson : définition, moyenne, variance, autocorrélation
   - Signal du télégraphiste : non-stationnarité, version stationnaire, autocorrélation, densité spectrale
