---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407448"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una estructura [DTBLPAGE](dtblpage.md) para describir un control de página con pestañas, una etiqueta de una longitud especificada y una entrada de archivo de ayuda de una longitud especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> Longitud de la etiqueta de la pestaña de página.
    
_n1_
  
> Longitud de la entrada que aparece en el archivo Mapisvc.inf que identifica el archivo de ayuda que se usará con el control de página con fichas.
    
_s_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La **macro SizedDtblPage** permite definir un control de página con pestañas cuando se conoce el número de caracteres de la etiqueta asociada y la entrada del archivo de ayuda. La nueva estructura se crea con los siguientes miembros: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Para usar un puntero a la estructura resultante de la macro **SizedDtblPage** como puntero de estructura **DTBLPAGE,** realice la conversión siguiente: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Vea también

- [DTBLPAGE](dtblpage.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

