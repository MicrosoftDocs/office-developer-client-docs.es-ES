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
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823305"
---
# <a name="sortkey-cell-shape-data-section"></a>Celda SortKey (sección Datos de formas)

Da como resultado una cadena que influye en el orden en el que se presentan los elementos en la ventana **Datos de formas**. 
  
## <a name="remarks"></a>Comentarios

El cálculo que se usa para comparar los valores de SortKey es específico de configuración regional y no distingue mayúsculas de minúsculas. Si los valores de SortKey son iguales, los datos de formas se muestran en orden de fila. Datos de formas que no tienen ningún criterio de ordenación se enumeran después de datos de formas que contienen una clave de ordenación.
  
El siguiente es un ejemplo del uso de claves de orden para mostrar los datos de formas en la ventana **Datos de formas** según el orden: Número de artículo, Cantidad, Precio. 
  
 *Fila, etiqueta* y *SortKey* hacen referencia a celdas de la fila de datos de formas. En este caso, las filas de datos de forma nombradas. 
  
|**Row**|**Label**|**SortKey**|
|:-----|:-----|:-----|
| Prop.Item  <br/> | Número de elemento  <br/> | 1  <br/> |
| Prop.precio  <br/> | Precio  <br/> | 3  <br/> |
| Prop.Quan  <br/> | Cantidad  <br/> | 2  <br/> |
   
Para obtener una referencia a la celda SortKey por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | De propiedades.  *Nombre* . SortKey donde de propiedades.  *Nombre* es el nombre de la fila de propiedad personalizada  <br/> |
   
Para obtener una referencia desde un programa a la celda SortKey por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsSortKey** <br/> |
   

