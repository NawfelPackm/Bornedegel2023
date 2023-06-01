API REST pour la borne de gel hydroalcoolique

Cette API permet de stocker et de récupérer les données suivantes de la borne de gel hydroalcoolique :

ID de la carte ESP32, 
Niveau de gel,
Niveau de batterie,
Lieu où est installée la borne de gel

Utilisation

Pour utiliser cette API, vous devez envoyer une requête HTTP POST avec les paramètres suivants :

esp32_id : l'ID de la carte ESP32

niveau_gel : le niveau de gel de la borne de gel (en %)

niveau_batterie : le niveau de batterie de la borne de gel (en %)

salle : le lieu où est installée la borne de gel

Vous pouvez envoyer la requête en utilisant un outil de requête HTTP tel Postman.

Exemple de requête

Voici un exemple de requête HTTP POST pour envoyer les données de la borne de gel :

URL : http://51.210.151.13/btssnir/projets2023/bornegel/

Paramètres : application/content type

Exemple esp32_id=86&niveau_gel=90&niveau_batterie=25&salle=1

Si la requête est envoyée avec succès, l'API renvoie une réponse HTTP 200 OK avec le message suivant :

Enregistrement effectué avec succès.

Si une erreur se produit lors de l'enregistrement des données dans la base de données, 
l'API renvoie une réponse HTTP 500 avec un message d'erreur.
