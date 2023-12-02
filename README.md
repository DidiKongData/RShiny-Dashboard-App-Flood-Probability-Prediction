# RShiny-Dashboard-App-Flood-Probability-Prediction
## Application RShiny Dashboard - Simulation d'un Processus Stochastique de Poisson
Cette plateforme a pour but d'afficher de manière interactive et dynamique des visualisations graphiques de données relativement au projet de simulation du cours de 'Techniques de Simulation' à l'ISFA.
<img width="934" alt="image" src="https://github.com/DidiKongData/RShiny-Dashboard-App-Flood-Probability-Prediction/assets/147708254/2b04c63c-f50b-44a1-993a-f45f4927492a">
# WARNING - DISCLAIMER !
L'existence de cette plateforme en particulier relève uniquement de mon intérêt personnel de vouloir apprendre en profondeur les librairies 'Shiny' et 'ShinyDashboard' de R, ainsi que de créer une application permettant à une tierce personne de pouvoir naviguer simplement à travers les différents résultats de simulations. La réalisation de cette application n'a absolument pas été demandé ni requis dans le cadre du projet scolaire, dont l'unique but était de pouvoir réussir les simulations mais pas de créer une application.

### TOUS DROITS RÉSERVÉS
### Dinesh BALASOUPRAMANIANE
ISFA 2023/2024

# Projet principal (la création de l'application n'est pas dans le projet)
1.1 Contexte
On considère le fleuve Coulantine traversant la ville d’Aussec. On souhaite savoir
quelle est la probabilité que ce fleuve déborde et inonde la ville au cours de l’année 2024,
selon qu’on construise ou non des murets autour de son lit.
On modélise les pluies par un ensemble de dates où elles tombent (on considère
ces pluies instantanées), et des intensités pour chacune de ces dates. À partir de ces
données, aléatoires, un modèle nous permet de calculer la hauteur d’eau dans le fleuve à
tout moment de l’année, et donc tester si la hauteur maximale dépasse un certain seuil
correspondant au début d’une inondation.
1.2 Dates des pluies
On modélise les dates des pluies par un processus de Poisson inhomogène, de fonction intensité λ définie par
λ(t) = λ0(1 + α sin(4πt)),
où λ0 et α sont des constantes du modèle, vérifiant λ0 > 0 et 0 ≤ α < 1. Dans cette
expression, t représente le temps en années, avec t = 0 au début de l’année 2024 et t = 1
à la fin de l’année 2024.
On note T1, T2, . . . les variables aléatoires correspondant aux dates des pluies.
1.3 Intensité des pluies
On modélise les intensités de chacune des pluies par des variables aléatoires indépendantes, et indépendantes des dates des pluies, toutes de loi PI de densité fI définie
par
fI (x) = 1R+
(x)
cI
m + |x − x0|
η
,
où cI est une constante de normalisation, et m > 0, x0 > 0 et η > 2 sont des paramètres
du modèle.
On note I1, I2, . . . les variables aléatoires correspondant aux intensités des pluies.
1.4 Hauteur d’eau
La hauteur d’eau H(t) dans le fleuve Coulantine au temps t est définie comme suit :
H(t) = ∑
i≥1
Ii × r(t − Ti),
1
où r est la fonction de résorption de l’eau de ce fleuve :
r(t) = 1R+
(t) exp(−vt)
en notant v la vitesse de résorption.
On notera Hmax la hauteur maximale de l’eau dans le fleuve Coulantine au cours de
l’année 2024 :
Hmax = max
0≤t≤1
H(t).
2 Résultat attendu
On cherche à approximer, par une méthode de Monte Carlo, la probabilité que Hmax
dépasse le seuil h0 (donné) correspondant à l’inondation de la ville d’Aussec :
p
∗
(h0) = P [Hmax > h0] .
<img width="934" alt="image" src="https://github.com/DidiKongData/RShiny-Dashboard-App-Flood-Probability-Prediction/assets/147708254/a35adcde-231e-4fea-a6a3-f8103fd29eed">
<img width="960" alt="image" src="https://github.com/DidiKongData/RShiny-Dashboard-App-Flood-Probability-Prediction/assets/147708254/2e624e40-b309-4fd5-bdc8-bbcb9b00d58c">
<img width="960" alt="image" src="https://github.com/DidiKongData/RShiny-Dashboard-App-Flood-Probability-Prediction/assets/147708254/af7331be-eed0-4c28-a5ea-108b89092303">
<img width="960" alt="image" src="https://github.com/DidiKongData/RShiny-Dashboard-App-Flood-Probability-Prediction/assets/147708254/9356b5c4-8f93-4393-8481-48dd04dffd47">
<img width="938" alt="image" src="https://github.com/DidiKongData/RShiny-Dashboard-App-Flood-Probability-Prediction/assets/147708254/1f2f1021-d435-469a-8118-1504d0ad0783">
<img width="946" alt="image" src="https://github.com/DidiKongData/RShiny-Dashboard-App-Flood-Probability-Prediction/assets/147708254/30dc3d7f-cabd-445f-b42f-3f9e23975fb4">


