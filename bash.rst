Bash
====

Agir suivant la valeur d'une variable
-------------------------------------

.. code-block:: bash

	# Pour comparer des chaînes de caractères, 
	# utiliser == au lieu de -eq
	if [ $i -eq 0 ]
	then
		# actions à réaliser si $i est égal à 0
	else
		# actions à réaliser si $i n'est pas égal à 0
	fi

Passer un paramètre
-------------------

.. code-block:: bash

	echo "Nombre de paramètres passés au script : $#"
	echo "Premier paramètre : $1"
	echo "Deuxième paramètre : $2"

Récupérer la sortie d'une commande
----------------------------------

*Récupérer dans une variable, ce que la commande affiche dans le terminal.*

.. code-block:: bash

	output=$(pwd)
	echo "Vous êtes dans le répertoire $output"

Lire un fichier ligne par ligne
-------------------------------

..
	https://unix.stackexchange.com/questions/169716/why-is-using-a-shell-loop-to-process-text-considered-bad-practice

.. code-block:: bash

	# read n'est pas fait pour cela, mais dans ce contexte
	# on se permet de l'utiliser ...
	cat /etc/network/interfaces | while read ligne
	do
		echo "Ligne lue : $ligne"
	done

Affiche : 

.. code-block::

	Ligne lue : auto lo
	Ligne lue : iface lo inet loopback
	Ligne lue : auto eth0
	Ligne lue : iface eth0 inet dhcp

Lire la valeur de retour d'une commande
---------------------------------------

.. code-block:: bash

	rm fichier.txt
	# Affiche 0 si le fichier a bien été supprimé par rm
	# ou 1 dans le cas contraire
	echo $?

Boucler sur les valeurs dans un intervalle
------------------------------------------

.. code-block:: bash

	for i in {10..20}
	do
		echo "La valeur de i est : $i"
	done

Patienter un certain temps
--------------------------

.. code-block:: bash

	# Dormir 60 secondes
	sleep 60
	# Dormir 30 millisecondes
	sleep 0.03
