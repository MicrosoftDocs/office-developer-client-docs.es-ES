---
title: GETVAL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Obtiene el valor de una celda y no recalcula la fórmula cuando cambia el valor de la celda.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416891"
---
# <a name="getval-function"></a>Función GETVAL

Obtiene el valor de una celda y no recalcula la fórmula cuando cambia el valor de la celda.
  
## <a name="syntax"></a>Sintaxis

GETVAL (* * *cellname* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre de la celda de la cual obtener el valor.  <br/> |
   
## <a name="example"></a>Ejemplo

GETVAL(PinX) + GETVAL(PinY) + Width 
  
Devuelve la suma de los valores de las celdas PinX, PinY y Width. 
  

