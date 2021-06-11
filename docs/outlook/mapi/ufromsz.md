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
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439012"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte una cadena terminada en null de dígitos decimales en un entero sin signo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Puntero a la cadena terminada en null que se va a convertir. El  _parámetro lpsz_ no debe superar los 65536 caracteres. 
    
## <a name="return-value"></a>Valor devuelto

 **UFromSz** devuelve un entero sin signo. Si la cadena no comienza con al menos un dígito decimal, se devuelve cero. 
  
## <a name="remarks"></a>Comentarios

La **función UFromSz** deja de convertir cuando alcanza el primer carácter de la cadena que no es un dígito decimal. Por ejemplo, teniendo en cuenta la cadena "55", **UFromSz** devuelve el valor entero 55. Dada la cadena "5a5b", la función devuelve el valor entero 5. Dada la cadena "a5b5", **UFromSz** devuelve cero. 
  
 **UFromSz es** sensible a las diferencias diacríticos. Se admiten cadenas en los formatos Unicode y DBCS. El límite de longitud de  _lpsz_ está en caracteres, no necesariamente bytes. 
  

