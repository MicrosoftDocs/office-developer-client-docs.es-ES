---
title: Celda SortKey (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Da como resultado una cadena que influye en el orden en el que se presentan los elementos en la ventana Datos de formas.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417857"
---
# <a name="sortkey-cell-shape-data-section"></a>Celda SortKey (Sección de datos de formas)

Da como resultado una cadena que influye en el orden en el que se presentan los elementos en la ventana **Datos de formas**. 
  
## <a name="remarks"></a>Comentarios

El cálculo que se utiliza para comparar los valores de SortKey depende de la configuración regional y no distingue entre mayúsculas y minúsculas. Si los valores de SortKey son iguales, los datos de formas aparecen según el orden de las filas. Los datos de formas que no tienen ningún criterio de ordenación se muestran después de los datos de forma que contienen un criterio de ordenación.
  
El siguiente es un ejemplo del uso de claves de orden para mostrar los datos de formas en la ventana **Datos de formas** según el orden: Número de artículo, Cantidad, Precio. 
  
 *Row, Label* y *SortKey* hacen referencia a celdas de la fila de datos de formas. En este caso se ha asignado un nombre a las filas de datos de formas. 
  
|**Row**|**Label**|**Criterio**|
|:-----|:-----|:-----|
| Prop. Item  <br/> | Número de elemento  <br/> | 1  <br/> |
| Prop. Price  <br/> | Precio  <br/> | 3  <br/> |
| Prop. Quan  <br/> | Cantidad  <br/> | segundo  <br/> |
   
Para obtener una referencia a la celda SortKey por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Polyprop.  *Nombre* . SortKey donde prop.  *Nombre* es el nombre de la fila de propiedades personalizadas  <br/> |
   
Para obtener una referencia desde un programa a la celda SortKey por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsSortKey** <br/> |
   

