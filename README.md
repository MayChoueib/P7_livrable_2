# P7 - Implémentez un modèle de scoring- OpenClassroom-Parcours Data Scientist 

---------

L’entreprise « prêt à dépenser », qui propose des crédits à la consommation pour des personnes ayant peu ou pas du tout d'historique de prêt, souhaite développer un modèle de scoring de la probabilité de défaut de paiement du client pour étayer la décision d'accorder ou non un prêt à un client potentiel en s’appuyant sur des sources de données variées (données comportementales, données provenant d'autres institutions financières, etc.).
## Mission
•	Construire un modèle de scoring qui donnera une prédiction sur la probabilité de faillite d'un client de façon automatique.
•	Construire un dashboard interactif à destination des gestionnaires de la relation client permettant d'interpréter les prédictions faites par le modèle et d’améliorer la connaissance client des chargés de relation client.
Ce projet est découpé en trois parties:  
## 1. Partie modélisation
•	Code P7_modelisation : Ce fichier contient le code de la modélisation du prétraitement des données à la prédiction et les interprétations globales et locales via SHAP en passant par l’étape importante de feature engineering.  
•	Les fonctions utilisées sont disponibles dans le module p7_functions     
## 2. Partie API (data_api.py)   
•	Réalisé avec Flask et hébergé par Heroku   
•	Dépôt Github : https://github.com/MayChoueib/P7_api_heroku_git    
•	 Lien vers l’API sur heroku : https://maychoueib-credit-score-api.herokuapp.com/   
•	 L’API contient les end-points suivants pour interagir avec le Dashboard « front-end»:   
-	Chargement des numéros des clients et leurs données   
-	Prédiction du score et décision   
-	Informations descriptives des clients   
-	Les clients similaires (20 plus proches voisins)  
-	Interprétation globale et locale (SHAP)  
## 3. Partie Dashboard Streamlit (st-dashboard.py)  
•	Code réalisé avec Streamlit et hébergé sur leur cloud   
•	Dépôt Github : https://github.com/MayChoueib/P7_dashboard_streamlit  
•	Lien vers le Dashboard https://maychoueib-p7-dashboard-streamlit-st-dashboard-hlfoen.streamlitapp.com/  
•	En appelant l’API, ce Dashboard affiche :  
-	Choix d'un numéro de demande dans menu déroulant   
-	Décision pour le crédit (accepté ou refusée) et le score sur une jauge   
-	Importance globale et locale des caractéristiques dans la décision du modèle   
-	Comparaison du client avec d’autres clients au choix dans un menu déroulant, un groupe des clients ou seulement les clients similaires :    

*Case à cocher : Représentation en boxplot des clients selon leur classe (crédit accepté ou rejeté) et place le client selon la couleur de sa classe (rouge ou vert)*   
*Case à cocher : Une analyse bi-variée interactive des caractéristiques à choisir dans 2 listes déroulantes et plaçant le client sur la courbe*    


Sources :    
•	[1] Lien détail du projet 7 OPENCLASSROOMS : https://openclassrooms.com/fr/projects/632/assignment   
•	[2] Lien Kernel Kaggle utilisé : https://www.kaggle.com/willkoehrsen/start-here-a-gentle-introduction   
•	[3] Lien téléchargement des données : https://www.kaggle.com/c/home-credit-default-risk/data   

