---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820691"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Hace referencia a**: Outlook 
  
Crea una estructura con nombre que incluye una estructura [DTBLLABEL](dtbllabel.md) para describir un control de etiqueta y la etiqueta asociada de una longitud especificada. 
  
|||
|:-----|:-----|
|Especificado en el archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Parámetros

_n_
  
> Longitud de la etiqueta. Esto incluye el carácter nulo final. 
    
_s_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedDtblLabel** le permite definir una etiqueta de tabla para mostrar cuando se conoce el número de caracteres en la etiqueta. Se crea la nueva estructura con los siguientes miembros: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Para utilizar un puntero a la estructura resultante de la macro **SizedDtblLabel** como un puntero de estructura **DTBLLABEL** , realizar la conversión a la siguiente: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Vea también

- [DTBLLABEL](dtbllabel.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

