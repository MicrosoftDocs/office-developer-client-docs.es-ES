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
ms.openlocfilehash: f5cb63ca3d421073b00a448f762ecf0137494f2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818417"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Se aplica a**: Outlook 
  
Esta función es similar a **WideCharToMultiByte**, que se asigna una cadena de UTF-16 (carácter ancho) a una nueva cadena de caracteres. La nueva cadena de caracteres no está necesariamente desde un carácter de varios bytes establecida.
  
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

## <a name="parameters"></a>Sintaxis

 _uCodePage_
  
> [entrada] Página de códigos a utilizar para realizar la conversión.
    
 _dwFlags_
  
> [entrada] Marcas que indica el tipo de conversión.
    
 _lpWideCharStr_
  
> [entrada] Puntero a la cadena Unicode para convertir.
    
 _cchWideChar_
  
> [entrada] Marcas que indica el tipo de conversión.
    
 _lpMultiByteStr_
  
> [out] Opcional. Puntero a un búfer que recibe la cadena convertida.
    
 _cchMultiByte_
  
> [entrada] Tamaño, en bytes, del búfer indicado por _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Opcional. Puntero al carácter que se va a usar si no se puede representar un carácter en la página de código especificado.
    
 _lpfUsedDefaultChar_
  
> [out] Opcional. Puntero a una marca que indica si la función ha usado un carácter predeterminado en la conversión.
    
## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes escritos en el búfer al que señala por _lpMultiByteStr_ si se realiza correctamente. 
  
## <a name="remarks"></a>Notas

Esta función ajusta la función **WideCharToMultiByte** . Para obtener más información, vea [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Ver también



[WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

