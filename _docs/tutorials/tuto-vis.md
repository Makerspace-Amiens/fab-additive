---
layout: documentation
image: image.png
hide_hero: false
hero_image: image.png
hero_darken: true
component_toc: true
doc_header: true
type: none

title: Assemblage : Quel vis choisir ?
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

todo: 10
---

## 1. À quoi servent les vis CHC, BHC et FHC ?

Dans un projet de prototypage mécanique, le choix du bon type de vis influe directement sur la solidité, l’esthétique, et la facilité de montage. Au MakerSpace, il y a trois types de vis :

- **CHC** : Tête Cylindrique Hexagonale Creuse (classique, robuste, encastrable)
- **BHC** : Tête Bombée Hexagonale Creuse (esthétique, peu encombrante)
- **FHC** : Tête Fraisée Hexagonale Creuse (affleurante, finition propre)

Ce guide vous aide à choisir le bon type de vis selon votre situation et vous indique comment les intégrer correctement dans vos conceptions.

## 2. Tableau de comparaison rapide

| **Type de vis** | **Forme de tête**         | **Avantages**                                                               | **Quand l'utiliser ?**                                               | **Conseils de modélisation 3D / laser**                                             |
|----------------|----------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **CHC**        | Tête cylindrique droite    | Serrage fort, robuste, bonne tenue dans le temps                          | Assemblage solide, structure méca, boîtier technique                 | Lamage cylindrique (diamètre tête + 0.2 mm), profondeur tête. Trou traversant.     |
| **BHC**        | Tête bombée basse          | Esthétique, non agressive, profil bas, pas de fraisage nécessaire         | Pièces visibles, capots, zones manipulées, faible épaisseur          | Trou traversant (diamètre vis + 0.2 mm), pas de fraisage. Attention au diamètre tête.|
| **FHC**        | Tête conique fraisée       | Montage affleurant, finition lisse, centrage automatique                  | Face visible, surface plane, boîtier fini, contact avec d’autres objets | Trou fraisé à 90° (angle standard), diamètre tête + 0.2 mm, profondeur tête.         |

## 3. Rappel sur les dimensions usuelles

| Filetage | Trou de passage | Ø Tête CHC | Ø Tête BHC | Ø Tête FHC | Profondeur tête CHC | Profondeur tête FHC |
|----------|------------------|------------|------------|------------|----------------------|----------------------|
| M3       | 3.2 mm           | ~5.5 mm    | ~6.0 mm    | ~6.0 mm    | ~3 mm               | ~2 mm               |
| M4       | 4.2 mm           | ~7.0 mm    | ~8.0 mm    | ~8.0 mm    | ~4 mm               | ~2.5 mm             |
| M5       | 5.2 mm           | ~8.5 mm    | ~9.5 mm    | ~9.5 mm    | ~5 mm               | ~3 mm               |

Ces valeurs sont indicatives. Toujours vérifier les dimensions exactes de vos vis avant modélisation.

## 4. Conseils généraux pour le design

- **Ajoutez une marge de +0.2 mm** au diamètre de passage pour le jeu de montage.
- Pour les CHC, **modélisez un lamage cylindrique** avec la bonne profondeur.
- Pour les FHC, utilisez la fonction de **fraisure à 90°**.
- Les BHC sont souvent utilisées **sans logement**, mais attention à leur plus grand diamètre.
- **Testez vos tolérances** sur une pièce témoin avant impression finale.

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
