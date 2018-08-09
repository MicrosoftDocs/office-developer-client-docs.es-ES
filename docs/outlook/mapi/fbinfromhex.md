---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816811"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Hace referencia a**: Outlook 
  
Convierte una representación de cadena de un número hexadecimal en datos binarios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Parámetros

 _sz_
  
> [entrada] Puntero a la cadena de ASCII terminada en null que se va a convertir. No es una cadena Unicode. Los caracteres válidos incluyen los caracteres hexadecimales cero a través de nueve y ambos caracteres en mayúsculas y minúsculas A la f el.
    
 _pb_
  
> [out] Puntero al número binario devuelto.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La cadena se ha convertido correctamente en un número binario. 
    
FALSE 
  
> La cadena de entrada contiene caracteres no válidos de hexadecimal de ASCII.
    
## <a name="see-also"></a>Vea también



[ScBinFromHexBounded](scbinfromhexbounded.md)

