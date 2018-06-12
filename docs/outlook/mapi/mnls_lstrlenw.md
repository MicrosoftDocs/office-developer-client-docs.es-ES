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
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818428"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Se aplica a**: Outlook 
  
Determina la longitud de la cadena Unicode especificada, excluyendo el carácter nulo.
  
> [!TIP]
> Considere la posibilidad de usar [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) en su lugar. 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Sintaxis

 _lpsz_
  
> [entrada] La cadena Unicode terminada en null que se va a comprobar.
    
## <a name="return-value"></a>Valor devuelto

La función devuelve un número entero con la longitud de la cadena. Es un recuento de caracteres en la cadena, excepto el carácter nulo. Si _lpsz_ es NULL, la función devuelve cero. 
  
## <a name="remarks"></a>Notas

Esta función ajusta la función **lstrlen** . Para obtener más información, vea [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Ver también



[lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

