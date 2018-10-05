---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Última modificación: 21 de febrero de 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392091"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Determina la longitud de la cadena Unicode especificada, excluyendo el carácter nulo.
  
> [!TIP]
> Considere la posibilidad de usar [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) en su lugar. 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parámetros

 _lpsz_
  
> [entrada] La cadena Unicode terminada en null que se va a comprobar.
    
## <a name="return-value"></a>Valor devuelto

La función devuelve un número entero con la longitud de la cadena. Es un recuento de caracteres en la cadena, excepto el carácter nulo. Si _lpsz_ es NULL, la función devuelve cero. 
  
## <a name="remarks"></a>Comentarios

Esta función ajusta la función **lstrlen** . Para obtener más información, vea [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Vea también



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

