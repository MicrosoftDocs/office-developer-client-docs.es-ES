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
ms.openlocfilehash: 5be5cd7c352201159c0257861c0072b56da65082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820927"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Hace referencia a**: Outlook 
  
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
  

