---
layout: documentation
image: Bambu_Printers.png  
hide_hero: true  
hero_image: Bambu_Printers.png    
hero_darken: true  
component_toc: true  
doc_header: true
type: tuto_printers

title: Bambulab A1 Mini, P1P & X1C 
subtitle: Imprimer une pièce sur les Bambulab 
description: Dans ce tutoriel, vous apprendrez à imprimer sur les machines de la marque BambuLab (Rack de gauche en entrant dans le PrinterLab) en utilisant le logiciel OrcaSlicer.  
author: Rémi Lacombe

time: 3  
difficulty: 2  
compatibilities-os: win, mac, lin

softwares: 
  - label: OrcaSlicer  
    link: ""

todo: 100  
---

# Impression 3D d'une pièce

Ce **tutoriel d'initiation** vous guidera de l'**exportation** de votre modèle jusqu'a la **fin de l'impression**, en vous aidant à éviter les erreurs courantes.

Avant de débuter ce tutoriel, nous supposons que votre pièce **a déjà été conçue et exportée sur une clé USB** au format **.STL**, **.3MF** ou **.STEP** depuis votre logiciel de CAO (OnShape, Solidworks, FreeCAD, Fusion 360...).

{% include message.html 
   title="Pour le faire dans OnShape :" 
   message="Dans le volet **Pièces** en bas à gauche, **sélectionnez la ou les pièces** que vous souhaitez **exporter** :
   ![Select](Select_Part.png)  
   Clique droit sur la sélection, puis **Exporter**  
   ![alt text](Export.png)  
   Dans le menu d'exportation qui s'ouvre, nommez votre fichier, et sélectionnez le format de sortie.
   Pour un rendu optimal, nous conseillons l'export en **.STEP**  
   ![alt text](Export_Window.png)  
   Mettez finalement le fichier téléchargé sur une **clé USB**.

   " 
   status="is-info" 
   dismissable="false" 
   icon="fas fa-exclamation-cube" 
%}

Si votre modèle n'est pas encore créé, rendez-vous sur la page [**tutoriels CAO**](/pages/tutoriels-cao).

{% include step-tuto.html  
greyBackground = true  
image = "Etagere_Bambu.jpg"  
title="1 - Préparation et vérification"  
content="Vous vous trouvez maintenant au [**PrinterLab**](/pages/informations), un espace dédié à l'impression 3D au sein du MakerSpace. Vous y trouverez de nombreux modèles d'imprimantes, mais pas de panique, il suffit de suivre les étapes de ce tutoriel ;).

Nous nous concentrerons ici sur l'étagère de gauche en entrant, elle acceuille les imprimantes de la marque bambulab, c'est ici que votre pièce prendra forme !"  
%}

{% include step-tuto.html  
greyBackground = true  
image = "Powered_Bambu_A1_Mini.jpg"  
image_2 = "Spool.jpg"  
content="**Sélectionnez** la machine sur laquelle vous imprimerez votre pièce. Elle doit être **disponible** et **allumée**.

- Pour des pièces **inférieures à 18 cm** (dans toutes les dimensions) → utilisez les **A1 mini**  
- Pour des pièces **plus grandes** ou nécessitant plus de volume → utilisez les **P1P**  
- Pour des pièces **complexes** ou du **multi-couleurs** → utilisez la **X1 Carbon (X1C)**  

Vérifiez également que le **plateau d'impression** est **propre**, qu'il reste du **filament** et qu'il s'agit bien de **PLA**."  
%}

{% include message.html title="En cas de bobine vide" message="Suivez ce [**tutoriel**](/tutorials/3d-print/change-bobine/) pour la recharger." status="is-info" dismissable="true" icon="fas fa-duotone fa-cube" %}

{% include step-tuto.html  
greyBackground = true  
image = "USB_Port.png"
image_2 = "Landing_Page_Orca.png"
title="2 - Importation de votre pièce"  
content="Sur l'un des postes du PrinterLab, branchez votre clé dans l'embase USB devant l'écran.

Ouvrez le logiciel **OrcaSlicer** ![OrcaSlicer icon](Orca_Icon.png). OrcaSlicer est un logiciel de **tranchage** qui transforme les modèles 3D en instructions détaillées pour les imprimantes 3D.

Sur la page d'accueil, cliquez sur **New Project**.

![Nouveau Projet Orca](New_Project.png)"  
%}

{% include step-tuto.html  
greyBackground = true  
image = "Empty_File.png"  
content="En haut du volet de gauche, dans le **menu déroulant Printer**, **sélectionnez la machine choisie plus tôt**.

![Choix imprimante](Model_Choice_Menu.png)"  
%}

{% include step-tuto.html  
greyBackground = true  
image = "Benchy_On_Plate.png"  
content="Dans le **ruban supérieur**, cliquez sur le bouton **Ajouter** ![Ajouter](Add_Part.png) et sélectionnez votre **pièce** dans l'**explorateur de fichiers**.

Après validation, votre modèle devrait **apparaître au centre du plateau.**"  
%}

{% include step-tuto.html  
greyBackground = true  
image = "Benchy_On_Plate_Close_Up.png"  
title="3 - Paramètres d'impression"  
content="Dans le menu déroulant **Filament** sur le panneau de gauche, sélectionnez **Bambu PLA Basic**.

![Menu filament](Filament_Choice_Menu.png)"  
%}

{% include step-tuto.html  
greyBackground = true  
image = "Brim.png"  
content="Pour garantir l'adhérence de la pièce sur le plateau d'impression, rendez-vous sur le panneau **Others** dans le volet gauche.  
Dans le menu déroulant **Brim type**, sélectionnez **Outer brim only**.

![Menu bordure](Brim_Choice_Menu.png)

Augmentez ensuite la **largeur de la bordure** en passant le paramètre **Brim width** à **5 mm**.

Pour de très petites pièces, préférez une valeur proche de **10 mm**.

![Paramètre bordure](Brim_Param.png)"  
%}

{% include message.html title="Attention" message="Une imprimante ne peut imprimer dans le vide. Si votre pièce présente des surplombs importants, vous devrez cocher la case **Enable support** dans l'onglet **Support**. Si vous avez un doute, référez-vous à ce [**guide sur les supports en impression 3D**](https://all3dp.com/1/3d-printing-support-structures/) ou demandez conseil à un **fab manager**." status="is-warning" dismissable="true" icon="fas fa-exclamation-triangle" %}

{% include step-tuto.html  
greyBackground = true  
image = "Sliced_Benchy.png"  
content="Cliquez ensuite sur ![Slice plate](Slice_Plate.png) en haut à droite de la fenêtre.

Vous devriez maintenant voir votre **pièce tranchée** en couches. Le **temps d'impression** et la **matière consommée** s'affichent également sur le volet de droite.

![Temps et matière](Time_And_Material.png)

Vous pouvez visualiser le processus d'impression en utilisant le slider à droite.

![Simulation d'impression](Print_Slider.gif)"  
%}

{% include step-tuto.html  
greyBackground = true  
image = "Window.png"  
content="Avant de lancer l'impression, vérifiez que :  
- L'impression finira bien **avant l'heure de fermeture du MakerSpace** (consultez un **fab manager**).  
- La machine que vous avez choisie est **toujours disponible**.  
- Le plateau d'impression est **vide et propre**. Si ce n'est pas le cas, des **lingettes** et du produit de nettoyage (alcool isopropylique) sont à votre disposition sur le coté de la servante rouge.

![Nettoyage](Cleaning_Gear.jpg)

"

%}

{% include step-tuto.html  
greyBackground = true  
title="4 - Lancement de l'impression"  
image = "Window.png"  
content="Vous pouvez maintenant cliquer sur le bouton ![Imprimer](Print_Plate.png) en haut à droite de la fenêtre.

Dans le volet déroulant, sélectionnez l'imprimante choisie plus tôt.

![Choix imprimante](Printer_Choice_Menu.png)

Cliquez ensuite sur le bouton ![Envoyer](Send.png)

Après une phase de préchauffage et de calibration, l'imprimante réalise la **première couche**.

Pour garantir le **succès** de l'impression, il est crucial de contrôler que la matière **adhère** bien au plateau.

![En impression](Printing.gif)"
%}

{% include step-tuto.html  
greyBackground = true  
title="5 - Impression"  
image = "One_Eternity_Later.gif"  
content="Il faut maintenant laisser **l'imprimante faire son travail** !

Pour les longues impressions, il est important de vérifier régulièrement que tout se passe bien.

Si la **pièce se décolle** avant la fin ou qu'un **autre problème** survient, vous devrez **arrêter l'impression** depuis l'écran de l'imprimante.
"
%}

{% include step-tuto.html  
greyBackground = true  
title="6 - Post-traitement"  
image = "Remove_Part.gif"  
content="Après un peu de patience, voici votre **impression terminée** ! 

Pour **retirer la pièce du plateau**, pas besoin de forcer ! Il suffit d'attendre que le plateau refroidisse.

Après quelques minutes, soulevez et courbez légèrement le plateau, **sans le retirer**.

Si la pièce ne se décroche pas, **attendez quelques minutes** que le plateau refroidisse davantage."
%}

{% include step-tuto.html  
greyBackground = true  
image = "Remove_Brim_And_Trash_Bambu.gif"  
content="Retirez les **bordures** et **dépôts** de filament sur le plateau. Si vous avez activé l'option, **retirez également les supports**.

Jetez vos déchets dans la poubelle située à l'entrée du **PrinterLab**.

Assurez-vous de laisser votre espace de travail **propre** et **prêt** pour les prochains !"
%}

{% include step-tuto.html  
greyBackground = false  
image = "Benchy.png"  
content="Bravo ! Vous savez maintenant imprimer une pièce au **PrinterLab**.

Pour que ce lieu reste **ouvert à toutes et tous**, c'est maintenant à vous de **partager ce que vous avez** appris dans ce tuto !
"
%}

---

{%
  include card_collections.html
  title="Pour aller plus loin"
  description="Explorez d'autres tutoriels pour approfondir vos connaissances"
  type="tutorial"
%}