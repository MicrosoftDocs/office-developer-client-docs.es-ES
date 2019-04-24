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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327317"
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
  

