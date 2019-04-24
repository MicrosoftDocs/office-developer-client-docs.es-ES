---
title: Celda NoCoauth (sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede ser editado por varios autores de forma simultánea en una sesión de coautoría.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319442"
---
# <a name="nocoauth-cell-document-properties-section"></a>Celda NoCoauth (sección de propiedades del documento)

Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede ser editado por varios autores de forma simultánea en una sesión de coautoría.
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El documento no puede ser coautor y está bloqueado para edición al abrirlo.  <br/> |
|FALSE  <br/> |El documento puede ser coautor.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **NoCoauth** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | NoCoauth  <br/> |
   
Para obtener una referencia desde un programa a la celda **NoCoauth** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocNoCoauth** <br/> |
   

