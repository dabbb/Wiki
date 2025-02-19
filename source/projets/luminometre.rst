Luminometre
###########


Ce projet fait suite à la demande d'un bidouilleur d'Angers. Raphael, aveugle a exprimé le besoin d'avoir un boitier qui puisse lui communiquer l'intensité lumineuse via une vibration ou un buzzer.

Le besoin de développer ce genre d'appareil s'est fait car il semblerait que les solutions soient difficilement abordable ou alors indisponible.

:download:`Raphael a d'abord écris un document pour décrire ses besoins au niveau du luminomêtre. <../_static/luminometre.pdf>`


Les spécifications
------------------

Dans cette section on définie les différents points auxquels doit répondre le luminomètre.

* Détecter la luminosité ambiante
* Détecter la luminosité d'une diode ou du signal lumineux d'un appareil électrique.
* Donner l'information sur le niveau de luminosité via un signal sonore (entre 200Hz et 1500Hz, à définir avec l'utilisation).
* Donner l'information sur le niveau de luminosité via une vibration (la continuité de la vibration baisse en fonction de l'intensité lumineuse).
* L'utilisateur choisi le mode (buzzer/vibreur) via un bouton pour chaque mode, le luminomètre fonctionne uniquement quand les boutons sont pressés.
* Le luminomètre doit avoir la taille approximative d'un briquet être transportable.

Le 1er prototype
----------------

**Status** : En développement, il faut écrire le code qui tournera sur l'Attiny85

Le matériel choisi pour le prototype
====================================

* Une photorésistance, qui modifie la valeur de sa résistance en fonction de la luminosité, on part sur un `modele peu cher et utilisé dans beaucoup de projets <https://lcsc.com/product-detail/Photoresistors_Shenzhen-Jing-Chuang-He-Li-Tech-GL5516-5-10_C10077.html>`_
* 2 Boutons poussoir, 1 pour activer chaque mode
* `1 buzzer <https://lcsc.com/product-detail/Buzzers_Jiangsu-Huaneng-Elec-HMB1275-05B_C96491.html>`_
* `1 vibreur <https://www.adafruit.com/product/1201>`_
* 1 Attiny85, c'est un microprocesseur tout petit qui devrait pouvoir gerer tout les modes et generer le signal pour le vibreur et le buzzer
* 2 condensateurs de 100 nanofarad pour filtrer un peu les appui sur les boutons (on évite ainsi les rebonds)
* 1 résistance de 10KOhms à monter en série avec la photorésistance.

Le schéma électrique
====================

On passe par le logiciel EasyEDA, cela nous permet de rapidement produire le PCB une fois le schéma validé

.. figure :: ../_static/Schematic_Luminom-tre_Sheet-2_20190606191939.png

  le schema de principe du 1er prototype
