---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Última modificación: 20 de febrero de 2012'
ms.openlocfilehash: 3e23fa9fcb074fabacf1a2dd9ac3f632cdce5b5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576179"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos cadenas Unicode.
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>Parámetros

 _lcid_
  
> [entrada] Identificador de configuración regional. Para obtener definiciones detalladas, vea el parámetro de _Configuración regional_ de [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [entrada] Marcas para pasar por alto mayúsculas y minúsculas y diacríticos. Para obtener definiciones detalladas, vea el parámetro _dwCmpFlags_ de [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [entrada] Puntero a la primera cadena Unicode se va a comparar.
    
 _cch1_
  
> [entrada] Longitud en caracteres de la primera cadena Unicode, excluyendo el carácter nulo. La aplicación puede proporcionar un valor negativo si la cadena terminada en null. En este caso, la función **MNLS_CompareStringW** determina automáticamente la longitud. 
    
 _pstr2_
  
> [entrada] Puntero a la segunda cadena Unicode se va a comparar.
    
 _cch2_
  
> [entrada] Longitud en caracteres de la segunda cadena de Unicode, excluyendo el carácter nulo. La aplicación puede proporcionar un valor negativo si la cadena terminada en null. En este caso, la función determina automáticamente la longitud.
    
## <a name="return-value"></a>Valor devuelto

Devuelve los valores que se describen para [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Comentarios

Esta función ajusta [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** acepta los mismos parámetros y tiene el mismo comportamiento como [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Recursos adicionales



[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

