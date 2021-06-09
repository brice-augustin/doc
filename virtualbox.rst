VirtualBox
==========

Interface graphique
-------------------

La GUI de `VirtualBox` se compose de quatre zones :

#.	A gauche, la liste des VM actuellement gérées par l'hyperviseur
#.	A centre, les propriétés de la VM sélectionnée (CPU, RAM, disque dur, etc) 
#.	A droite, un *screenshot* de l’écran actuel de la VM
#.	En haut, les actions possibles sur la VM (démarrage, arrêt, clonage, etc)

.. _fig-vbox-gui:

.. figure:: images/vboxgui.png

	Interface de VirtualBox

Pour obtenir un affichage similaire à celui de la :numref:`fig-vbox-gui`, cliquez sur la VM, puis sur ``Machine Tools`` > ``Details``. 

Importer une VM
---------------

``Fichier`` > ``Importer un appareil virtuel`` > Sélectionner le fichier OVA à importer > ``Continuer``
Dans ``Politique d'adresse MAC``, sélectionner ``Générer de nouvelles adresses MAC pour toutes les interfaces réseau`` > ``Importer``

.. _fig-vbox-mac:

.. figure:: images/vbox-mac.png

	Réinitialisation de l'adresse MAC avant importation d'une VM

.. warning:: Vous devez systématiquement réinitialiser l'adresse MAC des cartes réseau d'une VM lors de l'importation. Dans le cas contraire, vous rencontrerez des problèmes de conflit d'adresses, et la communication entre VM ne pourra pas fonctionner !

Si vous avez oublié de le faire pendant l'importation, vous pouvez toujours :ref:`changer son adresse MAC<vbox-change-mac>` à n'importe quel moment. 

.. _vbox-change-mac:

Changer l'adresse MAC d'une VM
------------------------------

Pour changer l'adresse MAC d'une VM, il faut *obligatoirement* l'arrêter. 

Sélectionner la VM dans la fenêtre principale et cliquer sur ``Configuration`` pour afficher ses propriétés.
Dans la fenêtre des paramètres, sélectionner ``Réseau`` > ``Carte 1`` > ``Avancé`` > Cliquer sur le bouton de réinitialisation à droite de l'adresse MAC et valider. 

.. _fig-vbox-change-mac:

.. figure:: images/vbox-change-mac.png

	Changement de l'adresse MAC

Créer une VM
------------

Cliquer sur ``Nouvelle`` et suivre l'assistant de création. 
Si nécessaire, modifier les valeurs proposées (quantité de RAM, taille du disque, etc.), sinon laisser les valeurs par défaut. 

Insérer une image ISO dans le lecteur de CD (virtuel) d'une VM
--------------------------------------------------------------

Dans les caractéristiques de la VM, sélectionner ``Stockage`` > ``Contrôleur IDE``. 
Cliquer sur l'icône représentant un CD, puis sur ``Choisissez un fichier de disque optique virtuel`. 
Dans la fenêtre qui s'affiche, indiquer le fichier ISO. 


.. _fig-vbox-iso:

.. figure:: images/vbox-iso.png

	Choix d'un CD d'installation

Host Key
--------

La ``Host key`` est toujours indiquée en bas à droite de la fenêtre de l'hyperviseur. Pour ``VirtualBox``, il s’agit de la touche ``Ctrl`` située à droite du clavier.

.. _fig-vbox-hostkey:

.. figure:: images/vbox-hostkey.png

	Host key utilisée dans VirtualBox

Configurer la carte réseau d'une VM en mode ``Accès par pont``
--------------------------------------------------------------

Sélectionner la VM dans la fenêtre principale et cliquer sur ``Configuration`` pour afficher ses propriétés.
Dans la fenêtre des paramètres, sélectionner ``Réseau`` >``Carte 1`` > ``Accès par pont`` et valider. 
