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
description: Aplica la trama de línea, la trama de relleno o el final de línea denominado nombre a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o endArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337152"
---
# <a name="use-function"></a>Función USE

Aplica la trama de línea, la trama de relleno o el final de línea denominado _nombre_ a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow. 
  
## <a name="syntax"></a>Sintaxis

USE ("* * *Name* * *") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombre_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena de texto que sea un nombre de patrón válido.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Si un patrón denominado _nombre_ está presente en la galería de símbolos de documento del documento, el patrón se aplica como trama de línea, trama de relleno, flecha inicial o flecha final. 
  
Esta función siempre devuelve 254.
  
## <a name="example"></a>Ejemplo

USE("Líneas de tren") 
  
Aplica el patrón llamado Líneas de tren a la forma que contiene la fórmula para darle formato. 
  

