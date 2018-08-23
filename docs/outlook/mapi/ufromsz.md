---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7513e361f4c1c1bcc93cc420f3a1987e0d817c54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580505"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte una cadena terminada en null de dígitos decimales en un entero sin signo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parámetros

 _lpsz_
  
> [entrada] Puntero a la cadena terminada en null que se va a convertir. El parámetro _lpsz_ no debe superar los caracteres, de 65536. 
    
## <a name="return-value"></a>Valor devuelto

 **UFromSz** devuelve un entero sin signo. Si la cadena no comienza con al menos un dígito decimal, se devuelve cero. 
  
## <a name="remarks"></a>Comentarios

La función **UFromSz** detiene la conversión cuando alcanza el primer carácter en la cadena que no es un dígito decimal. Por ejemplo, dada la cadena "55", **UFromSz** devuelve el valor entero 55. Dada la cadena "5a5b", la función devuelve el valor entero 5. Dada la cadena "a5b5", **UFromSz** devuelve cero. 
  
 **UFromSz** es sensible a las diferencias diacríticas. Se admiten cadenas en los formatos de Unicode y DBCS. El límite de longitud de _lpsz_ es en caracteres, no necesariamente bytes. 
  

