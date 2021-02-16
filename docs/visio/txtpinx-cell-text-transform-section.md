---
title: Celda TxtPinX (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Determina la coordenada x del centro de rotación del bloque de texto en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423499"
---
# <a name="txtpinx-cell-text-transform-section"></a>Celda TxtPinX (Sección de transformación de texto)

Determina la coordenada  *x*  del centro de rotación del bloque de texto en relación con el origen de la forma. La fórmula predeterminada es: 
  
= Ancho \* 0,5
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda TxtPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtPinX  <br/> |
   
Para obtener una referencia desde un programa a la celda TxtPinX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormPinX** <br/> |
   

