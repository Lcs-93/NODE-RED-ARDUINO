# NODE-RED-ARDUINO
README du Flow Node-RED
Ce README fournit une vue d'ensemble et des instructions pour le flux Node-RED défini dans le fichier JSON fourni. Le flux semble contrôler un Arduino Uno via une communication série et dispose d'une interface utilisateur avec des curseurs, des boutons, des jauges et un modèle affichant une image.

Aperçu du Flux
Communication Série avec Arduino Uno

Le flux communique avec un Arduino Uno via le port série ("/dev/ttyACM0" avec un débit de 115200).
Composants de l'Interface Utilisateur (UI)

Curseur (Slider) : Contrôle l'intensité d'une LED.
Jauge 1 : Affiche l'intensité de la LED.
Jauge 2 : Représente une valeur de température.
Jauge 3 : Indique l'humidité.
Boutons (Rouge, Vert, Bleu) : Déclenchent des changements de couleur pour la LED.
Fonctions

Fonction 1 (function 1 led) :

Gère l'entrée du curseur et les pressions de bouton pour contrôler la couleur et l'intensité de la LED.
Envoie des commandes à l'Arduino Uno via la communication série.
Sortie d'informations de débogage.
Fonction 2 (function 2 temp) :

Analyse les données de température à partir de l'entrée série.
Met à jour une jauge pour afficher les informations de température.
Fonction 3 (function 3 humidité) :

Analyse les données d'humidité à partir de l'entrée série.
Met à jour une jauge pour afficher les informations d'humidité.
Débogage et Visualisation

Nœud de Débogage (debug 1) : Affiche des informations de débogage dans la barre latérale de débogage de Node-RED.
Interface Utilisateur

Un groupe d'interface utilisateur ("Group 1") contient les curseurs, les jauges et les boutons.
Un modèle d'image affiche une image du Accessory Shield V1.0.
Instructions
Configuration Arduino :

Connectez l'Arduino Uno à l'ordinateur via USB.
Assurez-vous que l'Arduino utilise le port série "/dev/ttyACM0" et un débit de 115200.
Installation de Node-RED :

Assurez-vous que Node-RED est installé sur votre système.
Importation du Flux :

Copiez le contenu du fichier JSON fourni.
Ouvrez Node-RED et importez le flux à l'aide de la fonction d'importation.
Configuration du Port Série :

Modifiez les nœuds "Arduino Uno" et "Arduino UNO in" pour correspondre à la configuration du port série de votre système.
Déploiement du Flux :

Déployez le flux importé dans Node-RED.
Accès à l'Interface Utilisateur :

Ouvrez le tableau de bord Node-RED pour interagir avec les curseurs, les boutons et les jauges.
Surveillance des Informations de Débogage :

Si nécessaire, activez le nœud de débogage ("debug 1") pour surveiller les informations de débogage dans la barre latérale de débogage de Node-RED.
Profitez de l'expérimentation avec le contrôle de la LED et la visualisation des données de capteurs !

Remarques Supplémentaires
Assurez-vous d'avoir les bibliothèques ou dépendances nécessaires installées dans Node-RED pour prendre en charge les nœuds utilisés dans ce flux.
Consultez la documentation officielle de Node-RED pour plus de détails sur l'utilisation de la plateforme : Documentation Node-RED.
