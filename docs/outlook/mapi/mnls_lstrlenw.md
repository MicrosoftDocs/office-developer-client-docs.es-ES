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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338468"
---
# <a name="mnls_lstrlenw"></a>MNLS_lstrlenW

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina la longitud de la cadena Unicode especificada, excluyendo el carácter nulo de terminación.
  
> [!TIP]
> Considere la posibilidad [de usar StringCchLength en](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) su lugar. 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parámetros

 _lpsz_
  
> [entrada] Cadena Unicode terminada en null que se va a comprobar.
    
## <a name="return-value"></a>Valor devuelto

La función devuelve un entero con la longitud de la cadena. Es un recuento de caracteres de la cadena, excepto el carácter nulo de terminación. Si  _lpsz_ es NULL, la función devuelve cero. 
  
## <a name="remarks"></a>Comentarios

Esta función ajusta la **función lstrlen.** Para obtener más información, [vea lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Consulte también



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

