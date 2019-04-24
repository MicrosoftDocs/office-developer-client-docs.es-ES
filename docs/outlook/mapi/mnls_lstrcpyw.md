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
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341730"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia una cadena en un búfer.
  
> [!CAUTION]
> No usar. Considere la posibilidad de usar [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) en su lugar. 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameters

lpString1
  
> contempla Un búfer para recibir el contenido de la cadena a la que señala el parámetro lpString2.
    
lpString2
  
> a Cadena terminada en null que se va a copiar.
    
## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un puntero al búfer.
  
Si se produce un error en la función, el valor devuelto es NULL y lpString1 no puede terminar en NULL.
  
## <a name="remarks"></a>Comentarios

Esta función ajusta la función **lstrcpy** . Para obtener más información, vea [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Vea también



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

