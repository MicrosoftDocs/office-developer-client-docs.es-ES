---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Última modificación: 21 de febrero de 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338734"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta función es similar a **WideCharToMultiByte**, que asigna una cadena UTF-16 (carácter ancho) a una nueva cadena de caracteres. La nueva cadena de caracteres no es necesariamente de un conjunto de caracteres multibyte.
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a>Parameters

 _uCodePage_
  
> a Página de códigos que se debe usar para realizar la conversión.
    
 _dwFlags_
  
> a Marcas que indican el tipo de conversión.
    
 _lpWideCharStr_
  
> a Puntero a la cadena Unicode que se va a convertir.
    
 _cchWideChar_
  
> a Marcas que indican el tipo de conversión.
    
 _lpMultiByteStr_
  
> [out] Opcional. Puntero a un búfer que recibe la cadena convertida.
    
 _cchMultiByte_
  
> a Tamaño, en bytes, del búfer indicado por _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Opcional. Puntero al carácter que se va a usar si un carácter no se puede representar en la página de códigos especificada.
    
 _lpfUsedDefaultChar_
  
> [out] Opcional. Puntero a una marca que indica si la función ha usado un carácter predeterminado en la conversión.
    
## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes escritos en el búfer al que apunta _lpMultiByteStr_ si se realiza correctamente. 
  
## <a name="remarks"></a>Comentarios

Esta función ajusta la función **WideCharToMultiByte** . Para obtener más información, vea [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Vea también



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

