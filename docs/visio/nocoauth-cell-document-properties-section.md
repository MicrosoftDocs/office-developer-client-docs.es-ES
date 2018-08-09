---
title: Celda NoCoauth (sección Propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede editarse por varios autores simultáneamente en una sesión de co-autoría.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822679"
---
# <a name="nocoauth-cell-document-properties-section"></a>Celda NoCoauth (sección Propiedades del documento)

Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede editarse por varios autores simultáneamente en una sesión de co-autoría.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El documento no se puede ser coautor y está bloqueado para su edición cuando se abre.  <br/> |
|FALSE  <br/> |Puede ser coautor del documento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **NoCoauth** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | NoCoauth  <br/> |
   
Para obtener una referencia a la celda **NoCoauth** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocNoCoauth** <br/> |
   

