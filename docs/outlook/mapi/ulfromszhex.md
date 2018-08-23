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
ms.openlocfilehash: e6de4be29811dafaf5288b2ccb39c0342a314bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584628"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte una cadena terminada en null de dígitos hexadecimales en un entero largo sin signo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parámetros

 _lpsz_
  
> [entrada] Puntero a la cadena terminada en null que se va a convertir. El parámetro _lpsz_ no debe superar los caracteres, de 65536. 
    
## <a name="return-value"></a>Valor devuelto

 **UlFromSzHex** devuelve un entero largo sin signo. Si la cadena no comienza con al menos un dígito hexadecimal, se devuelve cero. 
  
## <a name="remarks"></a>Comentarios

La función **UlFromSzHex** detiene la conversión cuando alcanza el primer carácter en la cadena que no es un dígito hexadecimal. Por ejemplo, dada la cadena "5a", **UlFromSzHex** devuelve el valor entero 90. Dada la cadena "5g5h", la función devuelve el valor entero 5. Dada la cadena "g5h5", **UlFromSzHex** devuelve cero. 
  
 **UlFromSzHex** es sensible a las diferencias diacríticas pero permite 'a' a 'f' y 'A' a 'F' de dígitos hexadecimales. Se admiten cadenas en los formatos de Unicode y DBCS. El límite de longitud de _lpsz_ es en caracteres, no necesariamente bytes. 
  

