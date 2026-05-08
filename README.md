# TP N°3 : Classification de SMS avec Deep Learning (LSTM) 🌌

[![Algorithme](https://img.shields.io/badge/Algorithme-LSTM_(RNN)-00f2ff.svg)](#)
[![Thème](https://img.shields.io/badge/Thème-Astronomic_Violet_Blue-8a2be2.svg)](#)
[![Framework](https://img.shields.io/badge/Framework-TensorFlow%20%2F%20Keras-ff6f00.svg)](#)

## 📌 Présentation du Projet

Ce troisième projet s'inscrit dans le module de Deep Learning et introduit le **Natural Language Processing (NLP)**. L'objectif est de construire un réseau de neurones capable de comprendre le langage humain pour classifier automatiquement des SMS en deux catégories : Légitimes (Ham) ou Indésirables (Spam).

Le rendu est un **compte rendu interactif monolithique (HTML/CSS/JS)** au design "Astronomic Violet Blue", intégrant la théorie mathématique complexe, le pipeline de traitement de texte, le code source Keras complet et les courbes d'évaluation dynamiques.

### 👥 Équipe de Réalisation
* **Auteurs :** Dahane Ahmed Lamine & Tabbi Meriem
* **Enseignante :** Mme. Fergani
* **Module :** Intelligence Artificielle / Deep Learning

---

## 🧠 Notions Fondamentales : Architecture LSTM

Les algorithmes classiques échouent sur du texte car ils ne comprennent pas le *contexte séquentiel*. Nous avons donc implémenté un **LSTM (Long Short-Term Memory)**, une variante avancée des Réseaux de Neurones Récurrents (RNN) qui évite le problème de la disparition du gradient grâce à un système de portes (Gates) mathématiques :
* **Forget Gate :** Décide quelle partie de la mémoire passée doit être effacée.
* **Input Gate :** Détermine quelles nouvelles informations du mot actuel méritent d'être stockées.
* **Output Gate :** Filtre la mémoire pour générer la prédiction et passer l'état au mot suivant.

---

## 🛠️ Le Pipeline NLP (Prétraitement)

Avant d'entrer dans le réseau de neurones, le texte subit un traitement mathématique rigoureux :
1. **Tokenisation :** Conversion de chaque mot en un entier unique (création d'un dictionnaire).
2. **Padding :** Normalisation de la taille des séquences (ajout de zéros pour que toutes les matrices aient la même forme, exigence stricte de Keras).
3. **Plongement Lexical (Word Embedding) :** Transformation des entiers en vecteurs denses spatiaux pour capturer les similarités sémantiques entre les mots.

---

## 📊 Évaluation et Métriques

Le modèle est évalué sur un jeu de test de 20% en utilisant des métriques de classification binaire :
* **Binary Crossentropy (Loss) :** Fonction de perte optimisée via Adam.
* **Accuracy :** Précision globale dépassant les 98%.
* **Couche Dropout (0.5) :** Utilisée avec succès pour empêcher le surapprentissage (Overfitting), comme le démontrent les courbes d'apprentissage superposées.

---

## 🚀 Utilisation

1.  **Installation :** Clonez le dépôt et assurez-vous d'avoir le fichier dataset `SMSSpamCollection` dans le même dossier.
2.  **Exécution Web :** Ouvrez simplement le fichier `tp3_lstm_spam.html` dans n'importe quel navigateur web moderne.
3.  **Visualisations :** Le rapport inclut des graphiques interactifs (Plotly.js) traçant l'**Évolution de la Perte** par époque et la **Matrice de Confusion**.

---
*Projet universitaire - Laboratoire IA - 2026*
