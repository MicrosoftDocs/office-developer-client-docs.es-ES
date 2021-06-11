---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433055"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte una cadena terminada en null de dígitos hexadecimales en un entero largo sin signo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Puntero a la cadena terminada en null que se va a convertir. El  _parámetro lpsz_ no debe superar los 65536 caracteres. 
    
## <a name="return-value"></a>Valor devuelto

 **UlFromSzHex** devuelve un entero largo sin signo. Si la cadena no comienza con al menos un dígito hexadecimal, se devuelve cero. 
  
## <a name="remarks"></a>Comentarios

La **función UlFromSzHex** deja de convertir cuando alcanza el primer carácter de la cadena que no es un dígito hexadecimal. Por ejemplo, teniendo en cuenta la cadena "5a", **UlFromSzHex** devuelve el valor entero 90. Dada la cadena "5g5h", la función devuelve el valor entero 5. Dada la cadena "g5h5", **UlFromSzHex** devuelve cero. 
  
 **UlFromSzHex** es sensible a las diferencias diacríticos, pero permite tanto 'a' a 'f' como 'A' a 'F' para dígitos hexadecimales. Se admiten cadenas en los formatos Unicode y DBCS. El límite de longitud de  _lpsz_ está en caracteres, no necesariamente bytes. 
  

