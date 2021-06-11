---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356857"
---
# <a name="mnls_isbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprueba que un puntero a una cadena ancha es válido.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Puntero a la cadena de caracteres ancho.
    
 _ucchMax_
  
> [in] Longitud máxima de la cadena en caracteres incluido el terminador.
    
## <a name="return-value"></a>Valor devuelto

Devuelve un valor Boolean que es true si la cadena es mala.
  
## <a name="remarks"></a>Comentarios

Esta función ajusta [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Para obtener más información, [vea IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

