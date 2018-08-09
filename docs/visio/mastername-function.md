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
description: Devuelve el nombre del patrón de una hoja como una cadena, o no devuelve la cadena 'ningún patrón' Si la hoja no tiene un patrón.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822587"
---
# <a name="mastername-function"></a>Función MASTERNAME

Devuelve el nombre del patrón de una hoja como una cadena, o devuelve la cadena "\<ningún patrón\>" si la hoja no tiene un patrón.
  
## <a name="syntax"></a>Sintaxis

MASTERNAME ([** *IdIdiomaOpc* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _IdIdiomaOpc_ <br/> |Opcional  <br/> |**Número** <br/> |Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Observaciones

Si el código de idioma indicado no es válido, se utiliza el idioma local. 
  

