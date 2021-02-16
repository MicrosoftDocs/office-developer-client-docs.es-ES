---
title: Celda UICode (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Determina el código de un campo insertado en versiones de Visio anteriores a Visio 2000.
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422218"
---
# <a name="uicode-cell-text-fields-section"></a>Celda UICode (Sección de campos de texto)

Determina el código de un campo insertado en versiones de Visio anteriores a Visio 2000.
  
## <a name="remarks"></a>Comentarios

Esta celda no aparece en la ventana ShapeSheet. Utilice esta celda si necesita solucionar algún problema de compatibilidad con versiones anteriores, como guardar un dibujo de Visio versión 2000 en el formato de archivo de Visio versión 5.0.
  
Para obtener una referencia a la celda UICode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Fields.UICod[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda UICode por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTextField** <br/> |
| Índice de fila:  <br/> |**visRowField**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visFieldUICode** <br/> |
   

