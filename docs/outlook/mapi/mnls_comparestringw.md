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
ms.openlocfilehash: f7889a255e2aa8ea4b6908f2f10a7b546a8ee3f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818396"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

