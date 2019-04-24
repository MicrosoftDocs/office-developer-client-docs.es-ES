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
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356850"
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

## <a name="parameters"></a>Parameters

 _lcid_
  
> a Identificador de la configuración regional. Para obtener definiciones detalladas, __ vea el parámetro locale de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> a Marcas para omitir mayúsculas y minúsculas y diacríticos. Para obtener definiciones detalladas, consulte el parámetro _dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> a Puntero a la primera cadena Unicode que se va a comparar.
    
 _cch1_
  
> a Longitud en caracteres de la primera cadena Unicode, excepto el carácter null de terminación. La aplicación puede proporcionar un valor negativo si la cadena termina en NULL. En este caso, la función **MNLS_CompareStringW** determina la longitud automáticamente. 
    
 _pstr2_
  
> a Puntero a la segunda cadena Unicode que se va a comparar.
    
 _cch2_
  
> a Longitud en caracteres de la segunda cadena Unicode, excepto el carácter null de terminación. La aplicación puede proporcionar un valor negativo si la cadena termina en NULL. En este caso, la función determina la longitud automáticamente.
    
## <a name="return-value"></a>Valor devuelto

Devuelve los valores descritos para [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Comentarios

Esta función ajusta [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** toma los mismos parámetros y tiene el mismo comportamiento que [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Vea también



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

