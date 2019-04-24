---
title: MASTERNAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Devuelve el nombre del patrón de una hoja como una cadena, o devuelve la cadena "sin patrón" si la hoja no tiene un patrón.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341800"
---
# <a name="mastername-function"></a>Función MASTERNAME

Devuelve el nombre del patrón de una hoja como una cadena o devuelve la cadena\<"sin\>patrón" si la hoja no tiene un patrón.
  
## <a name="syntax"></a>Sintaxis

MASTERNAME ([* * *ididiomaopc* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Ididiomaopc_ <br/> |Opcional  <br/> |**Number** <br/> |Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

Si el código de idioma indicado no es válido, se utiliza el idioma local. 
  

