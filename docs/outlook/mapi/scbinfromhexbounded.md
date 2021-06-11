---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439761"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte la parte especificada de una representación de cadena de un número hexadecimal en un número binario. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parameters

 _sz_
  
> [in] Puntero a la cadena terminada en null que se va a convertir. Los caracteres válidos incluyen los caracteres hexadecimales del 0 al 9 y los caracteres en mayúsculas y minúsculas de a f.
    
 _pb_
  
> [salida] Puntero al número binario devuelto.
    
 _cb_
  
> [in] Tamaño, en bytes, del _parámetro pb._ 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La conversión se ha realizado correctamente.
    
MAPI_E_CALL_FAILED
  
> Se encontraron caracteres no válidos.
    
## <a name="see-also"></a>Vea también



[FBinFromHex](fbinfromhex.md)

