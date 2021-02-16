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
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408148"
---
# <a name="displaylevel-cell-shape-layout-section"></a>Celda DisplayLevel (sección de diseño de la forma [Shape Layout])

Determina la banda del nivel de presentación (el intervalo relativo de la agrupación de orden Z) de la forma.
  
## <a name="remarks"></a>Comentarios

El orden Z es el orden de presentación de las formas en la página de dibujo. Una forma que se encuentra más arriba en el orden Z aparecerá delante de otra que se encuentra más abajo en el orden Z cuando una se superpone a la otra. 
  
El nivel de presentación divide las formas en agrupaciones o bandas. Todas las formas de una banda determinada tienen un orden Z superior al de las formas en la banda inferior. De manera predeterminada, la mayoría de las formas tiene un nivel de presentación igual a cero (0).
  
El intervalo de los niveles de presentación oscila entre -32.767 y +32.767. Las formas que tienen el mismo nivel de presentación se combinan en una única banda, donde también se clasificarán entre sí según el orden Z.
  
Puede cambiar el orden Z de las formas dentro de una banda mediante los comandos Traer **hacia** delante **,** Enviar hacia atrás **,** Traer al frente y Enviar al **fondo**. Si estos comandos mueven una forma fuera de su banda determinada, Microsoft Visio muestra el valor reservado -32768 en la celda DisplayLevel de la forma, a menos que la celda esté resguardada. En ese caso, la forma no se puede mover a una banda diferente y Visio muestra la advertencia "La protección de formas o las propiedades de capa impiden la ejecución completa de este comando". 
  
Para obtener una referencia desde otra fórmula a la celda DisplayLevel por su nombre, o desde un programa mediante la propiedad **CellsU**, use lo siguiente. 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |DisplayLevel  <br/> |
   
Para obtener una referencia desde un programa a la celda DisplayLevel por su índice, use la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLODisplayLevel** <br/> |
   

