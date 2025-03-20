# Speed_Dating_EDA
🏆 Speed Dating EDA - Analyse Exploratoire des Données



📌 Introduction

Ce projet est une analyse exploratoire des données (EDA) sur le Speed Dating, basée sur un dataset contenant les interactions entre des participants lors d'événements de speed dating.
L'objectif principal est de répondre à la question : Quels facteurs influencent la décision des participants d'accepter un second rendez-vous ?

L'objectif principal est de répondre à la question : Quels facteurs influencent la décision des participants d'accepter un second rendez-vous ?

📊 Données utilisées

Fichier : Speed Dating Data.csv

Nombre d'observations : Plusieurs centaines de participants

Attributs clés analysés :

attr_o : Attractivité perçue

fun_o : Niveau de fun perçu

intel_o : Intelligence perçue

sinc_o : Sincérité perçue

shar_o : Partage d’intérêts

career_c et field_cd : Carrière et domaine d’études

match : Indicateur de succès du speed dating

🔬 Méthodologie

L'analyse s'est déroulée en plusieurs étapes :

1. Nettoyage des données : Remplacement de certaines valeurs catégorielles pour améliorer les visualisations

2. Analyse descriptive: Visualisation des distributions d'âge, religion, la race, de la notation des attributs entre participants, le domaine d'études et les intentions de carrière
3. Analyse des facteurs influents: 
    - Corrélation entre les attributs (attractivité attr_o, amusant fun_o, même hobbies shar_o) et le match
    - Influence du domaine d'études et de la carrière
    - Différenciation entre hommes et femmes

    4. Test de significativité (Chi², p-values): Vérification des tendances statistiques (rejet de l'hypothèse nulle ?)

🎯 Résultats Principaux

✅ 1. L'Attractivité reste le critère dominant

L’attractivité perçue (attr_o) est le facteur le plus déterminant dans l’acceptation d’un second rendez-vous.
p-values pour attr_o :
Femmes (notées par les hommes) :
18-25 ans : p = 4.44e-38 (très significatif)
26-30 ans : p = 3.74e-16
31-35 ans : p = 2.46e-08
Hommes (notés par les femmes) :
18-25 ans : p = 3.08e-29
26-30 ans : p = 6.24e-26
31-35 ans : p = 1.32e-04
📌 Interprétation :
➡ Les hommes prennent encore plus en compte l’apparence physique que les femmes.
➡ L’effet de l’attractivité est significatif à tous les âges, mais diminue légèrement après 30 ans.

✅ 2. Le partage d’intérêts et le fun jouent aussi un rôle important

shar_o (partage d’intérêts) et fun_o (niveau de fun perçu) ont une corrélation significative avec le succès d’un match.
p-values pour shar_o :
18-25 ans : p = 9.05e-30
26-30 ans : p = 1.71e-14
31-35 ans : p = 1.25e-07
📌 Interprétation :
➡ Les intérêts communs sont particulièrement importants chez les jeunes hommes.
➡ Le fun est plus déterminant chez les jeunes (p < 0.05), mais perd en importance avec l'âge.

✅ 3. Les domaines d’études et carrières influencent différemment hommes et femmes

Test Chi² sur le domaine d’études (field_cd) :
p-value Hommes : 0.077 ❌ (pas significatif)
p-value Femmes : 8.06e-07 ✅ (très significatif)
➡ Les femmes sont plus influencées par le domaine d’études que les hommes.
➡ Exemple : Les femmes en sciences sociales ont des taux de match plus élevés.

Test Chi² sur la carrière (career_c) :
p-value Hommes : 0.044 ✅ (significatif)
p-value Femmes : 0.044 ✅ (significatif)
➡ La carrière influence les décisions des deux sexes, mais moins fortement que d’autres facteurs.


✅ 4. Les personnes qui surestiment leur attractivité ont un taux de match plus faible
📌 Les personnes qui surestiment leur attractivité (attr1_1 - attr_o > 1) ont un taux de match plus bas (19.36%) que celles qui sont réalistes (22.03%) ou qui se sous-estiment (23.44%).

📌 Mais elles obtiennent plus de matchs en absolu, car elles tentent plus d’opportunités.

➡ La confiance excessive peut être un frein au succès relatif, mais augmente le succès absolu en multipliant les tentatives.

🚀 Comment utiliser ce projet ?
Cloner ce dépôt GitHub :

git clone https://github.com/ton_utilisateur/Speed_Dating_EDA.git
cd Speed_Dating_EDA

pip install -r requirements.txt



📌 Améliorations futures
    - Construire un modèle prédictif pour anticiper le succès d'un match.


    📩 Contact
Si tu as des questions ou suggestions, n'hésite pas à me contacter via GitHub ! 😃
