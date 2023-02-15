RAPPORT DE FORENSIC 
=================
PREPARATION  
------------
Pour la preparation de l٬analyse forensic concernant le site web Bosch-cyber et l'attaque qui a eu lieu, je vais suivre les étapes suivantes:

*Collecte de données

*Analyse de la nature de l'attaque

*Examen des données exfiltrées

*faire une analyse étendue de l'attaque

*Développement d'un plan de remédiation

*faire le rapport d՚analyse

INTRODUCTION 
-----------
Ce rapport a pour objectif de présenter les résultats d'une analyse forensique sur l'attaque subie par le site web "bosch-cyber". Ce rapport se concentre sur les étapes de l'analyse effectuées pour identifier la nature de l'attaque, examiner les données exfiltrées et les méthodes utilisées pour compromettre le site. Ce rapport s'appuie sur les informations collectées à partir des logs du serveur web . Les résultats de cette analyse aideront à identifier les vulnérabilités exploitées par l'attaquant et à recommander des mesures de sécurité pour empêcher une telle attaque à l'avenir.

METHODOLOGIE 
------------
La méthodologie  utilisée pour mener a bien cette analyse forensique constitue  plusieurs étapes, chacune ayant pour but de répondre à des questions spécifiques sur l'attaque subie par le site web "bosch-cyber". Les étapes clés de l'analyse sont :

1.Examinez les logs du serveur web pour trouver des preuves d'activité suspecte, telle que des connexions sortantes vers des adresses IP inconnues.Pour ce faire nous allons utilisé les  commandes suivantes 
-

*tail -f /var/log/apache2/access.log :Cette commande affiche en temps réel les entrées les plus récentes du fichier de log d'accès d'Apache

*grep "client denied by server configuration" /var/log/apache2/error.log :pour afficher les entrées les plus récentes du fichier de log d'erreur d'Apache.  

2.analyser les fichiers de log du serveur web,pour ce faire nous allons utilisé les commandes suivantes:
-

*grep "error" /var/log/apache2/error.log :pour rechercher tous les messages d'erreur dans le fichier de log Apache qui peut etre du a une tentative d՚intuision

*grep "client denied by server configuration" /var/log/apache2/error.log :pour voire les adresses ip aui ont  tenter d՚avoir access au serveur et verifier s՚ils  appartiennent au reseau de l՚entreprise 

*grep "OUTBOUND" /var/log/apache2/access.log ։pour rechercher des connexions sortantes vers des adresses IP inconnues, vous pouvez utiliser la commande suivante

3.j ai utilise l outil ELK Stack : ELK (Elasticsearch, Logstash, Kibana) est un ensemble d'outils open source pour l'analyse de logs. Il nous permettra de collecter, d'analyser et de visualiser les logs en temps réel, ce qui peut aider à détecter les exfiltrations de fichiers.
-

RESULTATS
----------

CONCLUSIONS
-----------
RECOMMANDATIONS
-----------
CONCLUSION GENERALE 
------------
