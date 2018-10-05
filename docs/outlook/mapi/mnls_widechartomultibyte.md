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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385518"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

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
  
## <a name="remarks"></a>Comentarios

Esta función ajusta la función **WideCharToMultiByte** . Para obtener más información, vea [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Vea también



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

