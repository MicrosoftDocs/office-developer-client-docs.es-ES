---
title: Celda ShdwPattern (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Determina la trama de relleno para la sombra de una forma.
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823209"
---
# <a name="shdwpattern-cell-fill-format-section"></a>Celda ShdwPattern (sección Formato de relleno)

Determina la trama de relleno para la sombra de una forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Ninguno (relleno transparente)  <br/> |
|1  <br/> |Color de primer plano sólido  <br/> |
|2 - 40  <br/> |Varias tramas  <br/> |
   
## <a name="remarks"></a>Observaciones

Para establecer la trama de relleno, escriba un número entre 0 y 40, que corresponde al índice de la colección de tramas. También puede ver la colección de tramas de relleno en el cuadro de diálogo **Relleno** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Relleno** y, a continuación, en **Opciones de relleno**).
  
Para obtener una referencia a la celda ShdwPattern por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShdwPattern  <br/> |
   
Para obtener una referencia desde un programa a la celda ShdwPattern por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowFill** <br/> |
|Índice de celda:  <br/> |**visFillShdwPattern** <br/> |
   

