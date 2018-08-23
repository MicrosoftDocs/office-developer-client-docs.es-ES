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
ms.openlocfilehash: 87a470c1c682225eb1deefba9ccc8c12fbdc49c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569830"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[ScBinFromHexBounded](scbinfromhexbounded.md)

