---
title: USE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Se aplica la trama de línea, trama de relleno o extremo de línea llamado nombre a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823486"
---
# <a name="use-function"></a>USE (función)

Se aplica la trama de línea, trama de relleno o extremo de línea llamado _nombre_ a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow. 
  
## <a name="syntax"></a>Sintaxis

USE ("** *nombre* **") 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombre_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena de texto que sea un nombre de patrón válido.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Observaciones

Si un patrón con _nombre_ está presente en la Galería de símbolos de documento del documento, el patrón se aplica como patrón de línea, patrón de relleno, flecha inicial o flecha final. 
  
Esta función siempre devuelve 254.
  
## <a name="example"></a>Ejemplo

USE("Líneas de tren") 
  
Aplica el patrón llamado Líneas de tren a la forma que contiene la fórmula para darle formato. 
  

