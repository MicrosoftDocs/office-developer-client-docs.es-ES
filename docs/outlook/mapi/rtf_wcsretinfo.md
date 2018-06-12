---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820542"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Se aplica a**: Outlook 
  
Esta estructura proporciona información acerca de una secuencia en formato nativo devuelto desde descomprimir el cuerpo de un mensaje que se encapsula en el formato comprimido de texto enriquecido (RTF).
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Miembros

_tamaño_
  
> El tamaño de la estructura **RTF_WCSRETINFO** en número de bytes. 
    
_ulStreamFlags_
  
> Esto es un valor que indica el formato del cuerpo nativo. Este valor sólo es válida si el indicador **MAPI_NATIVE_BODY** se pasa en el parámetro _ulFlags_ de la estructura [RTF_WCSINFO](rtf_wcsinfo.md) que se pasa a la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Esto puede ser uno de los siguientes valores: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** , y el cuerpo es RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** , y el cuerpo tiene formato de texto sin formato.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** , y el cuerpo tiene formato de lenguaje de marcado de hipertexto (HTML).  <br/> |
   
## <a name="see-also"></a>Ver también

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

