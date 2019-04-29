---
title: Celda NonPrinting (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Habilita y deshabilita la impresión para la forma seleccionada.
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437262"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>Celda NonPrinting (sección de varios)

Habilita y deshabilita la impresión para la forma seleccionada.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Se deshabilita la impresión, pero la forma se mostrará en la ventana de dibujo.  <br/> |
| FALSE  <br/> | Se habilita la impresión.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede imprimir una guía si la selecciona y establece el valor de su celda NonPrinting en FALSE.
  
Para obtener una referencia a la celda NonPrinting por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | No imprimibles  <br/> |
   
Para obtener una referencia a la celda NonPrinting por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visNonPrinting** <br/> |
   

