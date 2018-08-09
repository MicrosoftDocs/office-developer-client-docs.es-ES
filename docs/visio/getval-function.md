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
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822226"
---
# <a name="getval-function"></a>Función GETVAL

Obtiene el valor de una celda y no recalcula la fórmula cuando cambia el valor de la celda.
  
## <a name="syntax"></a>Sintaxis

GETVAL (** *nombreDeCelda* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombreDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre de la celda de la cual obtener el valor.  <br/> |
   
## <a name="example"></a>Ejemplo

GETVAL(PinX) + GETVAL(PinY) + Width 
  
Devuelve la suma de los valores de las celdas PinX, PinY y Width. 
  

