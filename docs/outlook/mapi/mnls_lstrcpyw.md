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
ms.openlocfilehash: 2e4ae22ace37455c9ccb9d8ff2a7f07a48132234
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818411"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Se aplica a**: Outlook 
  
Copia una cadena en un búfer.
  
> [!CAUTION]
> No la use. Considere la posibilidad de usar en su lugar [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Sintaxis

lpString1
  
> [out] Un búfer para recibir el contenido de la cadena indicada por el parámetro lpString2.
    
lpString2
  
> [entrada] La cadena terminada en null que se va a copiar.
    
## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero en el búfer.
  
Si se produce un error en la función, el valor devuelto es NULL y lpString1 podrían no estar terminada en null.
  
## <a name="remarks"></a>Notas

Esta función ajusta la función **lstrcpy** . Para obtener más información, vea [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Ver también



[lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

