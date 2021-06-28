Alcatel 4018
============

.. _4018-menu:

Accéder au menu de configuration
--------------------------------

Câbler le téléphone, puis brancher l'alimentation électrique. 

Immédiatement après, appuyer simultanément sur les touches ``#`` et ``i`` à intervalle régulier, jusqu'à ce que l'écran affiche ``Password:``

Le mot de passe est ``000000``.

Touches de navigation (à droite de l'écran du téléphone) :

.. csv-table:: Touches de navigation
   :header: "Touche", "Rôle"
   :widths: 130, 130

	``ok``, "Valider"
	``Flèches haut`` et ``bas``, "Menu suivant/précédent"
	"Touche ``retour``", "Revenir en arrière/Annuler"

Configuration IP statique
-------------------------

..
	IP memory > Restore config > From memory(x) : marche pas pour reset conf

:ref:`Accéder au menu de configuration<4018-menu>` du téléphone, puis 

	``IP parameters`` > ``IP mode: Static``

En adressage statique, les paramètres suivants sont configurables. 
Les paramètres qui doivent recevoir un maximum d'attention de votre part sont marqués d'un ``***``. 

*Pour les autres paramètres, contentez-vous de vérifier que la valeur indiquée est bien configurée. Vous n'avez pas besoin de comprendre leur rôle pour réaliser la maquette.*

.. csv-table:: Paramètres de configuration IP
   :header: "Paramètre", "Rôle", "Valeur"
   :widths: 150, 250, 100

	``*** IP@``, "Adresse IP du téléphone", *Voir prépa*
	``*** Subnet``, "Masque", *Voir prépa*
	``*** Router``, "Passerelle par défaut", *Voir prépa*
	``Remote Work``, "?", "Décoché"
	``DL Scheme``, "Protocole utilisé pour télécharger la configuration du téléphone", ``tftp``
	``Use default port``, "Utiliser le port TFTP par défaut", "Décoché"
	``*** DL Addr``, "Adresse du serveur TFTP", "Adresse IP de l'IPBX"
	``DL Port``, "Port TFTP", ``69``
	``DL Path``, "?", *vide*
	``Use VLAN``, "Sans objet", "Décoché"
	``VLAN ID``, "Sans objet", "Sans objet"
	``Strict VLAN``, "Sans objet", "Décoché"
	``DHCP UserClass``, "Sans objet", "Décoché"
	``Class``, "Sans objet", "Sans objet"

Vous devez impérativement sauvegarder la configuration : à la fin du menu, sélectionnez ``Save`` et validez. 
Redémarrez le téléphone (Touche ``Retour``) pour prendre en compte les modifications. 
