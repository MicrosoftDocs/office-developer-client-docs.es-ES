---
title: Celda Calendar (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Determina el calendario utilizado cuando una fórmula de celda contiene información de fecha.
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421819"
---
# <a name="calendar-cell-miscellaneous-section"></a>Celda Calendar (Sección de varios)

Determina el calendario utilizado cuando una fórmula de celda contiene información de fecha.
  
## <a name="remarks"></a>Comentarios

Los valores posibles son: 0 (Occidental), 1 (Hijri árabe), 2 (Hebreo lunar), 3 (Calendario de Taiwán), 4 (Japonés imperial), 5 (Budista tailandés), 6 (Danki coreano), 7 (Saka), 8 (Transliteración al inglés) y 9 (Transliteración al francés). 
  
Para obtener una referencia a la celda Calendar por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Calendar  <br/> |
   
Para obtener una referencia desde un programa a la celda Calendar por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visObjCalendar** <br/> |
   

