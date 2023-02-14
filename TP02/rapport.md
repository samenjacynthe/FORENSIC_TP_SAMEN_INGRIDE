# H1 EXERCICE 
Dans le fichier .csv suivant je veux que tu me donne la somme des logements de l'année 2019 ayant pour nom commune canteleu.
voici le lien pour télécharger le fichier .csv
[title](https://www.swisstransfer.com/d/80d03fab-a71d-4e7f-8410-9e99ef4a7f50)

#SOLUTION 
Pour pouvoir faire cette exercice tu dois d٬abord accéder au fichier en suivant les commandes ci dessous
![alt text](csv.png)
voici les commandes 
1.awk -F, '$1=="Canteleu" && $2=="2019" {sum += $3} END {print "Total des logements en 2019 pour Canteleu : " sum}' consommation-annuelle-residentielle-par-adresse.csv
Cette commande utilise "awk" pour lire le fichier .csv et rechercher les lignes contenant le nom de la commune "Canteleu" dans la première colonne ($1) et l'année "2019" dans la deuxième colonne ($2). Elle somme ensuite les nombres de logements de la troisième colonne ($3). Finalement, la commande affiche la somme totale des logements pour l'année 2019 à Canteleu.


