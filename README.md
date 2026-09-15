# Prédiction du churn client – VoltEdge

## Présentation du projet

Ce projet est un cas d’étude de Machine Learning consacré à la prédiction du churn client pour **VoltEdge**, un fournisseur d’énergie fictif.

L’objectif est d’identifier les clients susceptibles de quitter l’entreprise afin de pouvoir mettre en place des actions de fidélisation ciblées.

La prédiction repose sur quatre caractéristiques clients :

- Âge
- Ancienneté client
- Consommation annuelle
- Nombre de factures impayées au cours de la dernière année

Un modèle de **régression logistique** a été utilisé afin d’estimer la probabilité de churn.



## Technologies utilisées

- Python
- pandas
- scikit-learn
- Jupyter Notebook



## Méthodologie

Le projet suit les principales étapes d’un workflow de classification :

1. Chargement et exploration des données
2. Analyse de la variable cible
3. Sélection des variables explicatives
4. Séparation des données en ensembles d’entraînement et de test
5. Entraînement du modèle de régression logistique
6. Évaluation du modèle
7. Prédiction de la probabilité de churn
8. Application du modèle à de nouveaux clients

Les données ont été divisées en :

- **80 % pour l’entraînement**
- **20 % pour le test**



## Performance du modèle

Le modèle de régression logistique obtient une précision de :

### **82,75 %**

Il réalise **331 bonnes prédictions sur 400**.

## Matrice de confusion

![Matrice de confusion](IMAGES/confusion_matrix.png)

La matrice montre que le modèle identifie correctement :

- **215 clients restés** ;
- **116 clients ayant quitté VoltEdge**.

Il produit également **30 faux positifs** et **39 faux négatifs**.

D’un point de vue métier, les faux négatifs sont particulièrement importants : ils correspondent à des clients qui quittent réellement l’entreprise mais que le modèle n’a pas identifiés comme étant à risque.



## Exemple de prédiction

Le modèle a également été utilisé pour estimer la probabilité de churn d’un client présentant le profil suivant :

- Âge : 25 ans
- Ancienneté : 6 mois
- Consommation annuelle : 15 000 kWh
- Factures impayées : 2

La probabilité de churn prédite est de :

### **99,60 %**

Ce client présente donc un risque de départ très élevé et pourrait faire partie des clients à cibler en priorité par une action de fidélisation.



## Interprétation métier

Le modèle constitue une première aide à la décision pour identifier les clients présentant un risque élevé de churn.

Avec une précision de **82,75 %**, il permet de classer correctement une grande partie des clients.



