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
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820561"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Hace referencia a**: Outlook 
  
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
    
## <a name="see-also"></a>Vea también



[FBinFromHex](fbinfromhex.md)

