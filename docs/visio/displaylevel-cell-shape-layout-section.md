---
title: Celda DisplayLevel (sección de diseño de la forma [Shape Layout])
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Determina la banda del nivel de presentación (el intervalo relativo de la agrupación de orden Z) de la forma.
ms.openlocfilehash: 516446b2d401aaca614e24a2c5bb5003fafe8574
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821967"
---
# <a name="displaylevel-cell-shape-layout-section"></a>Celda DisplayLevel (sección Diseño de forma)

Determina la banda del nivel de presentación (el intervalo relativo de la agrupación de orden Z) de la forma.
  
## <a name="remarks"></a>Observaciones

El orden Z es el orden de presentación de las formas en la página de dibujo. Una forma que se encuentra más arriba en el orden Z aparecerá delante de otra que se encuentra más abajo en el orden Z cuando una se superpone a la otra. 
  
El nivel de presentación divide las formas en agrupaciones o bandas. Todas las formas de una banda determinada tienen un orden Z superior al de las formas en la banda inferior. De manera predeterminada, la mayoría de las formas tiene un nivel de presentación igual a cero (0).
  
El intervalo de los niveles de presentación oscila entre -32.767 y +32.767. Las formas que tienen el mismo nivel de presentación se combinan en una única banda, donde también se clasificarán entre sí según el orden Z.
  
Puede cambiar el orden Z de las formas dentro de una banda mediante el uso de los comandos **Traer al frente**, **Enviar hacia atrás**, **Traer al frente**y **Enviar al fondo**. Si los comandos mover una forma fuera de su banda determinado, Microsoft Visio muestra el valor reservado -32768 en la celda de nivel de presentación de la forma, a menos que la celda está protegida. En ese caso, no se puede mover la forma a una banda diferente y, Visio muestra la advertencia "las propiedades de protección o capa de forma impiden la ejecución completa de este comando". 
  
Para obtener una referencia desde otra fórmula a la celda DisplayLevel por su nombre, o desde un programa mediante la propiedad **CellsU**, use lo siguiente. 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Nivel de presentación  <br/> |
   
Para obtener una referencia desde un programa a la celda DisplayLevel por su índice, use la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLODisplayLevel** <br/> |
   

