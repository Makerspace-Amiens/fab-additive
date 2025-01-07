---
layout: documentation
hide_hero: false
hero_image: "page_1_img_20.png"
hero_darken: true
image: "page_1_img_20.png"
component_toc: false
doc_header: true
type: course

title: Règles de conception et conseils
subtitle: Concevoir pour l'impression 3D
description: Un ensemble de règles et de conseils pour mieux concevoir à destination de l'impression 3D
author: Adrien Bracq

time: 2
difficulty: 1

prerequisites:
  - label: Aucun pré-requis nécessaire
    link: ""

todo: 10
---


{% include step-tuto.html 
greyBackground = true 
content="**Base Chamfers**

**Recommended Value**: ~0.3 mm (initial layer height + layer height)

To improve the accuracy of the base edges of your part, it is a good idea to add a small chamfer of ~0.3 mm to all the edges that will be in contact with the print surface. This will reduce the chance of a slightly over “squished” first layer creating a lip around the base of the part. This is only relevant if you will be printing your part without a brim. If you are printing with a brim you will need to use a deburring tool our hobby knife to remove the brim a and clean up the base of the part anyway. "
image="page_1_img_20.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Base Corners**

**Recommended Value**: R > 4 mm

For larger parts, it is recommended to round corners that are in contact with the printer’s build plate (print surface). Sharp corners result in the shrinking forces that happen as the part cools (warping) concentrating at one point, whereas rounded corners act to disperse these forces. The larger the radius of the curved corner, the better your chances of reducing warping should be, at least in theory. A corner radius of 4mm or more is recommended."
image="page_1_img_21.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Bridging**

**Recommended Value**: < 10 mm

Horizontal bridges without support should not be longer than 10 mm to avoid print defects and failures. Either build vertical structures into your model to support the bridge or enable printed supports during slicing.You may find that you can bridge much larger gaps depending on the material and layer height, but keeping bridges <10 mm is a good starting point."
image="page_1_img_22.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Clearance**

**Recommended Values**: 
- ~0.3 mm for loose fit
- ~0.15 mm for tight fit

When 3D printed parts will fit together, a clearance of ~0.3 mm for loose fit and  ~0.15 mm for tight fit mm is recommended to ensure a good fit. The required clearance may vary slightly depending on material and geometry."
image="page_1_img_23.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Emboss & Engrave (Horizontal)**

**Emboss**:
- Recommended: >0.9 mm wide (2x extrusion width) x <0.9 mm high
**Engrave**:
- Recommended: >0.5 mm wide x <0.9 mm deep (2x extrusion width)

To ensure embossed or engraved details on a vertical surface are resolved and visible, the line width should be at least twice your nozzle diameter in depth. They can be a little bit larger but will start to sag if they are too big."
image="page_1_img_24.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Emboss & Engrave (Vertical)**

**Emboss**:
- Recommended: >0.9 mm wide (2x extrusion width) x <2 mm high
**Engrave**:
- Recommended: >0.5 mm wide x <2 mm deep

To ensure embossed or engraved details on a horizontal surface are resolved the line width should be at least 0.5 mm wide for engraving and 0.9 mm wide for embossing. There is no limit on the height of the details, but modeling them 2 mm high will make the features clearly visible."
image="page_1_img_25.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Feature Size**

**Recommended Value**: >1.8 mm (4x extrusion width)

The minimum feature size for printed structures is 4 times your extrusion line width. A good rule of thumb for general modeling is making features no smaller than 1.8 mm.."
image="page_1_img_26.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Fillets**

**Recommended Value**: > ø1 mm

Fillets are a great way to remove sharp corners or relieve stress concentrations at sharp corners. However, it is not recommended to model downward facing fillets on 3D printed parts. Chamfers are a good alternative for downward facing edges that you may wish to soften. Downward facing fillets will not cause your print to fail, but that may come out with poor aesthetic/surface quality. "
image="page_1_img_27.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Hole Size**

**Recommended Value**: > ø2 mm

It is not recommended to model holes with a diameter of less than 2 mm to ensure they are resolved. If an accurately sized hole of any size is necessary, undersize the hole and drill it out to the proper tolerance."
image="page_1_img_28.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Holes (Horizontal)**

**Recommended Offset**: a ≈ 0.3 mm

In order to print horizontal holes with a better tolerance, it is recommended to model the additional features in the image where the offset distance a, is the layer height of your print. If you are using a small layer height like 100μm you should do 2*a. This will accommodate for any drooping that will occur in the steep overhang sections of printed horizontal holes and the “flattening” of the bottom of holes due to the stacked layer process."
image="page_1_img_29.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Overhangs**

**Recommended Value**: < 50°

To prevent layers from drooping or curling on printed overhangs, it is recommended to avoid printing unsupported overhangs at angles over 50° (measured from the vertical axis down). Overhang quality can also be material-dependent, so some materials may require support at lower angles than others."
image="page_1_img_30.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Pins**

**Recommended Value**: > ø1.8 mm (4x extrusion width)

In order to accurately resolve pins, their diameter should be at least four times the extrusion line width to ensure at least two full perimeters are printed, a good rule of thumb is ø1.8 mm. If functional pins are required in your model, it may be better to use store bought pins and model holes into both sides of the joint."
image="page_1_img_31.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Threads (Modeled)**

**Recommended Value**: > M5 or UNC #10

3D printing modeled threads can work well for larger thread sizes. It is not recommended to model threads smaller than M5 or UNC #10 so that they will function effectively. If you need threads smaller than M5 or #10, they should be added with post-processing techniques such as a thread tap, or heat set threaded inserts. DO NOT use modeled/printed threads for horizontal holes."
image="page_1_img_32.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Threads (Post-Process)**

- Tap: Model hole at 90% of thread diameter.
- Self-tap: Model hole at 96% of thread diameter.
- Heat-set inserts: Model hole at 98% of insert’s outer diameter.

Threads can be added in post-processing a few different ways. You can thread tap the hole, in which case model the hole at 90% of the thread diameter. You can self-tap the screw into an unthreaded hole, in which case model the hole at 96% of the thread diameter. You can also use heat-set inserts, in which case model the hole at 98% of the inserts outer diameter."
image="page_1_img_33.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Unsupported Edges**

**Recommended Value**: < 0.9 mm (2x extrusion width)

It is generally recommended to avoid printing unsupported, horizontal structures that are more than two extrusion line widths wide, a good rule of thumb is 0.9 mm. It is unlikely that larger unsupported edges will cause print failures, but they will cause serious cosmetic issues. If the structures are necessary for your model, altering print orientation and/ or enabling supports will make them printable."
image="page_1_img_34.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Unsupported Holes**

**Recommended Value**: Extrude 1 = layer height, Extrude 2 = layer height x 2

Without special design considerations, holes through unsupported bridges will not print successfully. This technique can be used to print such holes without adding supports to your model.

When designing your part, extrude two rectangles tangent to your hole

The first extrude should be as thick as the layer height you intend to print with

The second extrude should be twice the layer height you intend to print with

This technique can be a little tricky to visualize until you have tried it a few times."
image="page_1_img_35.png" %}

{% include step-tuto.html 
greyBackground = true 
content="**Wall Thickness**

**Recommended Value**: > 0.9 mm (2x extrusion width)

It is strongly recommended to model walls at least two extrusions wide, generally this will be 0.9 mm. Thinner walls can have issues printing successfully and will not be very strong. Perimeters are the greatest source of strength in a 3D printed part, so if strength is important it is recommended to make walls more than two perimeters thick. Increasing perimeters will need adjustments in both modeling and slicing."
image="page_1_img_36.png" %}

---

{%
  include card_collections.html
  title="Pour aller plus loin"
  description="Explorez d'autres formations pour approfondir vos connaissances"
  type="course"
%}
