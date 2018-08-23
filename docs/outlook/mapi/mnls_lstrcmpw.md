---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Última modificación: 18 de junio de 2012'
ms.openlocfilehash: 36e22c60b32242425335b122b66c2c77e376848b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580120"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos cadenas Unicode.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Parámetros

 _lpString1_
  
> [entrada] Puntero a la primera cadena Unicode se va a comparar.
    
 _lpString2_
  
> [entrada] Puntero a la segunda cadena Unicode se va a comparar.
    
## <a name="return-value"></a>Valor devuelto

Devuelve los valores que se describen para una llamada equivalente al **MNLS_CompareStringW** excepto CSTR_EQUAL. 
  
## <a name="remarks"></a>Comentarios

 _MNLS_lstrcmpW_ realiza una comparación mediante una llamada a [MNLS_CompareStringW](mnls_comparestringw.md) con una configuración regional de GetUserDefaultLCID, 0 para indicadores y -1 para cch1 y cch2. 
  
## <a name="see-also"></a>Recursos adicionales



[GetUserDefaultLCID](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

