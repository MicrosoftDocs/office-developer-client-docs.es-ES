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
description: Aplica el patrón de línea, el patrón de relleno o el nombre del extremo de línea llamado a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422827"
---
# <a name="use-function"></a>Función USE

Aplica el patrón de línea, el  patrón de relleno o el nombre del extremo de línea llamado a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow. 
  
## <a name="syntax"></a>Sintaxis

USE(" ** *name* ** ") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombre_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena de texto que sea un nombre de patrón válido.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Si un patrón con nombre  _de nombre_ está presente en la galería de símbolos del documento, el patrón se aplica como un patrón de línea, patrón de relleno, flecha de inicio o flecha final. 
  
Esta función siempre devuelve 254.
  
## <a name="example"></a>Ejemplo

USE("Líneas de tren") 
  
Aplica el patrón llamado Líneas de tren a la forma que contiene la fórmula para darle formato. 
  

