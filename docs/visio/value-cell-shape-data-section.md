---
title: Celda Value (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Contiene el valor del elemento de datos de formas tal como se especificó en el cuadro de diálogo Definir datos de formas.
ms.openlocfilehash: 5b373149360167585fc5a143ce9458703e219045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823513"
---
# <a name="value-cell-shape-data-section"></a>Celda Value (sección Datos de formas)

Contiene el valor del elemento de datos de formas tal como se especificó en el cuadro de diálogo **Definir datos de formas**. 
  
## <a name="remarks"></a>Comentarios

Los valores especificados en el cuadro de diálogo **Definir datos de formas** reemplazan las fórmulas escritas en esta celda. Esto se cumple aunque se use la función GUARD para proteger la fórmula. 
  
Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | De propiedades.  *Nombre* . Valor de propiedades donde.  *Nombre* es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsValue** <br/> |
   

