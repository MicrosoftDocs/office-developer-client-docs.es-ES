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
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282708"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una estructura [DTBLLABEL](dtbllabel.md) para describir un control de etiqueta y la etiqueta asociada de una longitud determinada. 
  
|||
|:-----|:-----|
|Especificado en el archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> Longitud de la etiqueta. Esto incluye el carácter NULL final. 
    
_u_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedDtblLabel** permite definir una etiqueta de tabla de visualización cuando se conoce el número de caracteres de la etiqueta. La nueva estructura se crea con los siguientes miembros: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Para usar un puntero a la estructura resultante desde la macro **SizedDtblLabel** como un puntero de estructura **DTBLLABEL** , realice la siguiente conversión: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Vea también

- [DTBLLABEL](dtbllabel.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

