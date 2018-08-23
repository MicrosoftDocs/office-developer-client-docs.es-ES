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
ms.openlocfilehash: 135db8d690d4d4bd610bd15893c358fedddb4605
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589283"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte la parte especificada de una representación de cadena de un número hexadecimal en un número binario. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parámetros

 _sz_
  
> [entrada] Puntero a la cadena terminada en null que se va a convertir. Los caracteres válidos incluyen los caracteres hexadecimales 0 a 9 y los caracteres en mayúsculas y minúsculas a la f.
    
 _pb_
  
> [out] Puntero al número binario devuelto.
    
 _cb_
  
> [entrada] Tamaño, en bytes, del parámetro _pb_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Conversión fue correcta.
    
MAPI_E_CALL_FAILED
  
> Se encontraron caracteres no válidos.
    
## <a name="see-also"></a>Recursos adicionales



[FBinFromHex](fbinfromhex.md)

