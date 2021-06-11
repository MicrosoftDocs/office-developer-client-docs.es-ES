---
title: Celda NoCoauth (sección Propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede ser editado por varios autores simultáneamente en una sesión de coautoría.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420517"
---
# <a name="nocoauth-cell-document-properties-section"></a>Celda NoCoauth (sección Propiedades del documento)

Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede ser editado por varios autores simultáneamente en una sesión de coautoría.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El documento no se puede coautor y se bloquea para su edición cuando está abierto.  <br/> |
|FALSE  <br/> |El documento puede ser coautor.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **NoCoauth** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | NoCoauth  <br/> |
   
Para obtener una referencia desde un programa a la celda **NoCoauth** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocNoCoauth** <br/> |
   

