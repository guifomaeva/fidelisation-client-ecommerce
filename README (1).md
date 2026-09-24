# Fidélisation client d'un site e-commerce : segmentation RFM, prédiction du churn et tunnel de conversion

**Auteure :** Guifo Maeva · **Outils :** Python (Pandas, Scikit-learn, Matplotlib), Excel, Google Colab

## Contexte

Un site e-commerce perd des clients. La direction veut savoir :
- qui sont ses meilleurs clients ;
- quels clients risquent de partir, et pourquoi ;
- à quelle étape du parcours d'achat le site perd des ventes.

Les données sont **simulées mais réalistes** : 3 000 clients, environ 27 000 commandes (2024 – 2025) et 30 000 visites du site (octobre – décembre 2025).

## Démarche

1. **Nettoyage des données** : doublons, valeurs manquantes, montants en texte, formats de dates, commandes annulées.
2. **Segmentation RFM** (Récence, Fréquence, Montant) : 6 segments de clients (Champions, Fidèles, Nouveaux, À risque, À surveiller, Perdus).
3. **Modèle prédictif de churn** : régression logistique et forêt aléatoire (Random Forest), évaluées sur un jeu de test.
4. **Analyse du tunnel de conversion** par appareil (mobile, ordinateur, tablette).
5. **Recommandations chiffrées**, restituées dans un tableau de bord Excel.

## Principaux résultats

| Analyse | Résultat |
|---|---|
| Segmentation | Les Champions (25 % des clients) génèrent **52 % du chiffre d'affaires** |
| Clients à risque | 483 anciens bons clients inactifs depuis plus d'un an, soit **18 % du CA historique** |
| Modèle de churn | **AUC de 0,91**, 88 % des départs détectés ; premier signal : l'espacement des commandes |
| Canal d'acquisition | Les clients venus par code promo influenceur partent le plus |
| Tunnel de conversion | Sur mobile, **42 %** des paiements commencés sont finalisés, contre **77 %** sur ordinateur |

## Recommandations

1. **Simplifier le paiement mobile** (paiement express, achat sans compte) : gain estimé d'environ **+77 000 € de CA par an**.
2. **Réactiver les clients À risque** avec une campagne personnalisée.
3. **Utiliser le score de churn chaque mois** pour agir avant le départ des bons clients.
4. **Revoir les partenariats influenceurs**, dont les clients sont les moins fidèles.
5. **Protéger les Champions** avec un programme de fidélité.

## Contenu du dépôt

| Fichier | Description |
|---|---|
| `Projet2_Fidelisation_Client.ipynb` | Notebook Python complet, commenté étape par étape |
| `Donnees_Brutes_Fidelisation.xlsx` | Données brutes (clients, commandes, sessions) |
| `Analyse_Fidelisation_Excel.xlsx` | Analyse et tableau de bord Excel, avec recommandations chiffrées |

## Lancer le projet

Ouvrir le notebook dans [Google Colab](https://colab.research.google.com) (Fichier > Importer un notebook), puis exécuter les cellules dans l'ordre et charger le fichier `Donnees_Brutes_Fidelisation.xlsx` quand il est demandé.
