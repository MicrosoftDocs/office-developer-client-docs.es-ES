---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426173"
---
# <a name="rtf_wcsretinfo"></a>RTF_WCSRETINFO

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta estructura proporciona información sobre una secuencia en formato nativo que se devuelve al descomprimir el cuerpo de un mensaje encapsulado en formato de texto enriquecido comprimido (RTF).
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Miembros

_size_
  
> El tamaño de la **RTF_WCSRETINFO** en número de bytes. 
    
_ulStreamFlags_
  
> Este es un valor que indica el formato del cuerpo nativo. Este valor solo es válido si la marca **MAPI_NATIVE_BODY** se pasa en el parámetro _ulFlags_ de la estructura RTF_WCSINFO que se pasa [a](rtf_wcsinfo.md) la función [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md) Este puede ser uno de los siguientes valores: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Este valor solo se usa si  _ulFlags_ incluye **MAPI_NATIVE_BODY** marca y el cuerpo es RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Este valor solo se usa si  _ulFlags_ incluye **la marca MAPI_NATIVE_BODY** y el cuerpo es formato de texto sin formato.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Este valor solo se usa si  _ulFlags_ incluye **la marca MAPI_NATIVE_BODY** y el cuerpo es formato html (Lenguaje de marcado de hipertexto).  <br/> |
   
## <a name="see-also"></a>Vea también

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

