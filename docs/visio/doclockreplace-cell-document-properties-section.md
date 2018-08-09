---
title: Celda DocLockReplace (sección Propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina si la forma de reemplazar la interfaz de usuario debe deshabilitarse para este documento.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822025"
---
# <a name="doclockreplace-cell-document-properties-section"></a>Celda DocLockReplace (sección Propiedades del documento)

Determina si la forma de reemplazar la interfaz de usuario debe deshabilitarse para este documento. 
  
|||
|:-----|:-----|
|TRUE  <br/> |El botón **Reemplazar forma** está atenuado en la interfaz de usuario.  <br/> |
|FALSE  <br/> |El botón **Reemplazar forma** está activo en la interfaz de usuario. Los usuarios pueden usar la característica de la forma de reemplazar en este documento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **DocLockReplace** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DocLocReplace  <br/> |
   
Para obtener una referencia a la celda **DocLocReplace** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |** visDocLockReplace ** <br/> |
   

