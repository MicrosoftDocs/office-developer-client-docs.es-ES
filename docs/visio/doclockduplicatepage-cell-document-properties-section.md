---
title: Celda DocLockDuplicatePage (sección Propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Determina si las páginas del documento se pueden duplicar, como un valor booleano.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439663"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>Celda DocLockDuplicatePage (sección Propiedades del documento)

Determina si las páginas del documento se pueden duplicar, como un valor booleano.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Los** duplicados en el menú contextual de la página y el método de automatización **Page.Duplicate** están deshabilitados.  <br/> |
|FALSE  <br/> |La página se puede duplicar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **DocLockDuplicatePage** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DocLockDuplicatePage  <br/> |
   
Para obtener una referencia desde un programa a la celda **DocLockDuplicatePage** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocLockDuplicatePage** <br/> |
   

