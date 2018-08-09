---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Última modificación: 20 de febrero de 2012'
ms.openlocfilehash: dd7d310c8e801ba1246a0ce948aced9fa6a1a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818405"
---
# <a name="mnlsisbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Hace referencia a**: Outlook 
  
Comprueba que un puntero a una cadena de caracteres ancho es válido.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Parámetros

 _lpsz_
  
> [entrada] Un puntero a la cadena de caracteres anchos.
    
 _ucchMax_
  
> [entrada] La longitud máxima de la cadena de caracteres incluido terminador.
    
## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo Boolean que es true si la cadena es incorrecta.
  
## <a name="remarks"></a>Comentarios

Esta función ajusta [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx). Para obtener más información, vea [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).
  

