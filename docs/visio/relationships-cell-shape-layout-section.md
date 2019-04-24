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
ms.openlocfilehash: b270366fe1045aea3d628150c82e7fd798fa21df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359972"
---
# <a name="relationships-cell-shape-layout-section"></a>Celda Relationships (sección de diseño de la forma [Shape Layout])

Almacena las relaciones entre contenedores, listas, llamadas y formas. 
  
## <a name="remarks"></a>Comentarios

 Microsoft Visio usa la celda Relationships para almacenar las relaciones que implican esta forma. Se usa una serie de funciones DEPENDSON, con los parámetros mostrados, para representar las relaciones con esta forma, tal y como refleja la siguiente tabla. 
  
|**Primer parámetro**|**Parámetros adicionales**|
|:-----|:-----|
|1  <br/> |Formas que son miembros de este contenedor.  <br/> |
|segundo  <br/> |Formas que son miembros de esta lista.  <br/> |
|3  <br/> |Llamadas asociadas con esta forma.  <br/> |
|4  <br/> |Contenedores de los que esta forma es miembro.  <br/> |
|2,5  <br/> |Lista de la que este elemento de lista es miembro.  <br/> |
|6,5  <br/> |Formas asociadas con esta llamada.  <br/> |
|0,7  <br/> |Contenedor en cuyo borde límite izquierdo se asienta esta forma.  <br/> |
|8,5  <br/> |Contenedor en cuyo borde límite derecho se asienta esta forma.  <br/> |
|9  <br/> |Contenedor en cuyo borde límite superior se asienta esta forma.  <br/> |
|metros  <br/> |Contenedor en cuyo borde límite inferior se asienta esta forma.  <br/> |
|12  <br/> |Lista a la que esta lista se superpone.  <br/> |
   
Para obtener una referencia a la celda Relationships por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Relaciones  <br/> |
   
Para obtener una referencia desde un programa a la celda Relationships por su índice, use la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLORelationships** <br/> |
   

