---
title: Celda DocLockReplace (sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina si la interfaz de usuario reemplazar forma debe estar deshabilitada para este documento.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338608"
---
# <a name="doclockreplace-cell-document-properties-section"></a>Celda DocLockReplace (sección de propiedades del documento)

Determina si la interfaz de usuario reemplazar forma debe estar deshabilitada para este documento. 
  
|||
|:-----|:-----|
|TRUE  <br/> |El botón **reemplazar forma** está atenuado en la interfaz de usuario.  <br/> |
|FALSE  <br/> |El botón **reemplazar forma** está activo en la interfaz de usuario. Los usuarios pueden usar la característica reemplazar forma de este documento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **DocLockReplace** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DocLocReplace  <br/> |
   
Para obtener una referencia desde un programa a la celda **DocLocReplace** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |* * visDocLockReplace * * <br/> |
   

