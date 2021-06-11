---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356843"
---
# <a name="mnls_lstrcmpw"></a>MNLS_lstrcmpW

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos cadenas Unicode.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameters

 _lpString1_
  
> [in] Puntero a la primera cadena Unicode que se compara.
    
 _lpString2_
  
> [in] Puntero a la segunda cadena Unicode que se debe comparar.
    
## <a name="return-value"></a>Valor devuelto

Devuelve los valores descritos para una llamada equivalente a **MNLS_CompareStringW** excepto CSTR_EQUAL. 
  
## <a name="remarks"></a>Comentarios

 _MNLS_lstrcmpW_ realiza una comparación llamando a [MNLS_CompareStringW](mnls_comparestringw.md) con una configuración regional de GetUserDefaultLCID, 0 para las marcas y -1 para cch1 y cch2. 
  
## <a name="see-also"></a>Vea también



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

