---
layout: documentation
image: image.png
hide_hero: false
hero_image: tiroir_servante.jpg
hero_darken: true
component_toc: true
doc_header: true
type: tutorial

title: Assemblage, quel vis choisir ?
subtitle: Choisir entre CHC, BHC et FHC selon l’usage
description: Guide de sélection des vis pour le prototypage mécanique (impression 3D, découpe laser)
author: Rémi Lacombe

time: 1
difficulty: 1
compatibilities-os: win,mac,lin

prerequisites:
  - label: Aucun
    link: ""

softwares: 
  - label: Aucun
    link: ""

todo: 60
---

Dans un projet de **prototypage mécanique**, le choix du bon type de vis influe directement sur la **solidité**, **l’esthétique**, et la **facilité de montage**. Au MakerSpace, il y a **trois types de vis** :

{% include step-tuto.html 
title = "CHC : Tête Cylindrique"
greyBackground = true
content="

Les vis **CHC** (DIN 912) sont les plus courantes dans les assemblages mécaniques. Leur **tête cylindrique haute** avec empreinte hexagonale permet un **serrage fort** et une excellente tenue mécanique.

#### 📏 Dimensions standard

| Filetage (**d**) | Ø Tête (**dk**) | Hauteur tête (**k**) | Clé Allen (**s**) | Profondeur empreinte (**t**) |
|------------------|------------------|-----------------------|-------------------|-------------------------------|
| **M3**           | 5,5 mm           | 3,0 mm                | 2 mm              | 1,5 mm                        |
| **M4**           | 7,0 mm           | 4,0 mm                | 2,5 mm            | 2,0 mm                        |
| **M5**           | 8,5 mm           | 5,0 mm                | 4 mm              | 2,5 mm                        |
| **M6**           | 10,0 mm          | 6,0 mm                | 5 mm              | 3,0 mm                        |

#### ✅ Avantages

- **Serrage puissant** : parfait pour les pièces soumises à des efforts mécaniques.
- **Tête profonde** : l’empreinte hexagonale permet un bon maintien de la clé sans ripage.
- **Fréquemment utilisée** : compatible avec la majorité des composants mécaniques du commerce.
- **Encastrement facile** : tête cylindrique idéale pour créer un lamage simple.

#### 🧩 Intégration dans vos designs

##### 📌 Impression 3D

En impression 3D, il est recommandé de **modéliser un trou traversant + un lamage cylindrique** pour noyer la tête dans la pièce si nécessaire.

- M3 → trou de **3.2 mm**, lamage Ø **5.7 mm** × **3.0 mm**
- M4 → trou de **4.2 mm**, lamage Ø **7.2 mm** × **4.0 mm**
- M5 → trou de **5.2 mm**, lamage Ø **8.7 mm** × **5.0 mm**
- M6 → trou de **6.2 mm**, lamage Ø **10.2 mm** × **6.0 mm**

> Le lamage est important pour **éviter que la tête dépasse** ou interfère avec d’autres pièces.

##### 🔪 Découpe laser

Les CHC sont rarement encastrées dans des pièces découpées laser, mais on peut :
- soit **laisser la tête visible** (prévoir une surface dégagée),
- soit créer un **lamage en plusieurs couches** (stratégie sandwich ou collage de plaques).

Les trous peuvent être dessinés **au diamètre nominal**, car le **kerf laser** induit une tolérance suffisante :
- ex : 3.0 mm pour une vis M3, 4.0 mm pour une M4, etc.

> 💡 Astuce : si vous utilisez des CHC sur des pièces laser, pensez à **laisser un dégagement radial** autour du trou pour que la tête ne gêne pas d'autres éléments.

" 
image="CHC.png" %}


{% include step-tuto.html 
title = "BHC : Tête Bombée"
greyBackground = true
content="

Les vis **BHC** (DIN 7380) sont reconnaissables à leur **tête arrondie et basse**, avec une empreinte hexagonale creuse. Elles offrent un bon compromis entre tenue mécanique et aspect visuel soigné.

#### 📏 Dimensions standard

| Filetage (**d**) | Ø Tête (**dk**) | Hauteur tête (**dk**) | Clé Allen (**s**) | Profondeur empreinte (**t**) |
|------------------|------------------|----------------------|-------------------|-------------------------------|
| **M3**           | 5,7 mm           | 1,65 mm              | 2 mm              | 1,03 mm                       |
| **M4**           | 7,6 mm           | 2,2 mm               | 2,5 mm            | 1,3 mm                        |
| **M5**           | 9,5 mm           | 2,75 mm              | 3 mm              | 1,56 mm                       |
| **M6**           | 10,5 mm          | 3,3 mm               | 4 mm              | 2,08 mm                       |

#### ✅ Avantages

- **Esthétique** : la tête bombée donne un rendu propre, sobre, professionnel.
- **Profil bas** : plus discrète qu'une vis CHC, idéale si on veut éviter qu'une tête dépasse trop.
- **Agréable au toucher** : pas d’arête vive — on ne s’accroche pas dessus.
- **Pas de lamage nécessaire** : on peut les visser directement à la surface, pratique sur pièces fines.
- **Bonne surface d'appui** : répartit bien la pression sous la tête.

#### 🧩 Intégration dans vos designs

##### 📌 Impression 3D

En impression 3D, il est important de **prévoir une légère tolérance** dans les trous pour compenser la précision limitée du dépôt de matière (FDM). On recommande généralement :

- M3 → trou de **3.2 mm**
- M4 → trou de **4.2 mm**
- M5 → trou de **5.2 mm**
- M6 → trou de **6.2 mm**

Cela permet à la vis de s’insérer sans forcer, tout en assurant un bon maintien.

##### 🔪 Découpe laser

En découpe laser, **pas besoin d'ajouter de tolérance manuelle** :  
le **kerf** (la largeur du trait de coupe du laser) introduit naturellement un **jeu de l’ordre de 0.1 à 0.2 mm** selon le matériau utilisé.

→ Vous pouvez donc dessiner les trous **au diamètre nominal** de la vis (ex : 3.0 mm pour une M3)  
et obtenir un ajustement fonctionnel directement à la découpe.

> 💡 Astuce : si votre assemblage avec vis est un peu trop serré après découpe, un coup de lime ronde ou de foret manuel permet de corriger rapidement l’ajustement.

" 
image="BHC.png" %}

---

{% include message.html 
   title="Astuce" 
   message="Pensez à utiliser les fonctions 'trou avec lamage' ou 'trou fraisé' directement disponibles dans la plupart des logiciels de modélisation paramétrique pour gagner du temps et garantir la bonne géométrie." 
   status="is-info" 
   dismissable="false" 
   icon="fas fa-lightbulb" 
%}

---

{% include card_collections.html
  title="Pour aller plus loin"
  description="Découvrez aussi notre guide sur les inserts taraudés et l’utilisation des écrous encastrés."
  type="tutorial"
%}
