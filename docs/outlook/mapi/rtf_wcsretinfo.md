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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315788"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta estructura proporciona información acerca de una secuencia en formato nativo que se devuelve al descomprimir el cuerpo de un mensaje encapsulado en formato de texto enriquecido (RTF) comprimido.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Miembros

_size_
  
> El tamaño de la estructura **RTF_WCSRETINFO** en número de bytes. 
    
_ulStreamFlags_
  
> Se trata de un valor que indica el formato del cuerpo nativo. Este valor solo es válido si la marca **MAPI_NATIVE_BODY** se pasa en el parámetro _ulFlags_ de la estructura [RTF_WCSINFO](rtf_wcsinfo.md) que se pasa a la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Puede ser uno de los siguientes valores: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** y el cuerpo es RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** y el cuerpo es formato de texto sin formato.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** y el cuerpo es formato de lenguaje de marcado de hipertexto (html).  <br/> |
   
## <a name="see-also"></a>Vea también

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

