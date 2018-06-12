---
title: Celda Relationships (sección de diseño de la forma [Shape Layout])
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Almacena las relaciones entre contenedores, listas, llamadas y formas.
ms.openlocfilehash: c3410ad15581ff1704d7a43dd7ed5fa193f668b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822938"
---
# <a name="relationships-cell-shape-layout-section"></a>Celda Relationships (sección de diseño de la forma [Shape Layout])

Almacena las relaciones entre contenedores, listas, llamadas y formas. 
  
## <a name="remarks"></a>Observaciones

 Microsoft Visio usa la celda relaciones para almacenar las relaciones que implican esta forma. Una serie de funciones DEPENDSON, con los parámetros que se muestra, se utilizan para representar las relaciones con esta forma, tal como se muestra en la siguiente tabla. 
  
|**Primer parámetro**|**Parámetros adicionales**|
|:-----|:-----|
|1  <br/> |Formas que son miembros de este contenedor.  <br/> |
|2  <br/> |Formas que son miembros de esta lista.  <br/> |
|3  <br/> |Llamadas asociadas con esta forma.  <br/> |
|4  <br/> |Contenedores de los que esta forma es miembro.  <br/> |
|5  <br/> |Lista de la que este elemento de lista es miembro.  <br/> |
|6  <br/> |Formas asociadas con esta llamada.  <br/> |
|7  <br/> |Contenedor en cuyo borde límite izquierdo se asienta esta forma.  <br/> |
|8  <br/> |Contenedor en cuyo borde límite derecho se asienta esta forma.  <br/> |
|9  <br/> |Contenedor en cuyo borde límite superior se asienta esta forma.  <br/> |
|10  <br/> |Contenedor en cuyo borde límite inferior se asienta esta forma.  <br/> |
|11  <br/> |Lista a la que esta lista se superpone.  <br/> |
   
Para obtener una referencia a la celda Relationships por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Relaciones  <br/> |
   
Para obtener una referencia a la celda Relationships por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLORelationships** <br/> |
   

