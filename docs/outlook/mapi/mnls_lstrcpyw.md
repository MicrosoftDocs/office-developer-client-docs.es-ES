---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Última modificación: 18 de junio de 2012'
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575465"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia una cadena en un búfer.
  
> [!CAUTION]
> No la use. Considere la posibilidad de usar en su lugar [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Parámetros

lpString1
  
> [out] Un búfer para recibir el contenido de la cadena indicada por el parámetro lpString2.
    
lpString2
  
> [entrada] La cadena terminada en null que se va a copiar.
    
## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero en el búfer.
  
Si se produce un error en la función, el valor devuelto es NULL y lpString1 podrían no estar terminada en null.
  
## <a name="remarks"></a>Comentarios

Esta función ajusta la función **lstrcpy** . Para obtener más información, vea [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Recursos adicionales



[lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

