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
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431907"
---
# <a name="value-cell-shape-data-section"></a>Celda Value (Sección de datos de formas)

Contiene el valor del elemento de datos de formas tal como se especificó en el cuadro de diálogo **Definir datos de formas**. 
  
## <a name="remarks"></a>Comentarios

Los valores especificados en el cuadro de diálogo **Definir datos de formas** reemplazan las fórmulas escritas en esta celda. Esto se cumple aunque se use la función GUARD para proteger la fórmula. 
  
Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Prop.  *Nombre*  . Valor donde Prop.  *El*  nombre es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsValue** <br/> |
   

