---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344649"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta estructura permite especificar la información para descomprimir el cuerpo de un mensaje en formato comprimido de texto enriquecido (RTF) y, opcionalmente, devolver el flujo del cuerpo en su formato nativo.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>Miembros

 _size_
  
> El tamaño de la estructura **RTF_WCSINFO** en número de bytes. 
    
 _ulFlags_
  
> Es la máscara de las marcas de opción para la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Los indicadores de opción admitidos son: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Indica si el cliente pretende escribir la interfaz de secuencia ajustada que se devuelve.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Esto indica si se supone que el RTF descomprimido debe escribirse en la secuencia a la que apunta el puntero _lpCompressedRTFStream_ de la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .  <br/> |
|MAPI_NATIVE_BODY  <br/> |Esto indica si la secuencia descomprimida también se convierte en el cuerpo nativo antes de devolver la secuencia. Esta marca no se puede combinar con la marca **MAPI_MODIFY** .  <br/> |
   
 _ulInCodePage_
  
> Este es el valor de la página de códigos del mensaje. Normalmente, este valor se obtiene de la [propiedad canónica PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) en el mensaje. Este valor solo se usa cuando se pasa la marca **MAPI_NATIVE_BODY** en _ulFlags_. De lo contrario, este valor se omite.
    
 _ulOutCodePage_
  
> Este es el valor de la página de códigos del flujo descomprimido devuelto que desea. Si se establece en un valor distinto de cero, la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convierte la secuencia en la página de códigos especificada. Si se establece en un valor de cero, MAPI decide la página de códigos que se va a usar. Este valor solo se usa cuando la marca **MAPI_NATIVE_BODY** se pasa en _ulFlags_y el formato del cuerpo no es RTF. De lo contrario, este valor se omite.
    
## <a name="see-also"></a>Vea también



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

