---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Última modificación: 21 de febrero de 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338244"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Similar a **MultiByteToWideChar**, que asigna una cadena de caracteres a una cadena UTF-16 (carácter ancho). La cadena de caracteres no es necesariamente de un juego de caracteres multibyte.
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>Parameters

 _uCodePage_
  
> a Página de códigos que se debe usar para realizar la conversión.
    
 _dwFlags_
  
> a Marcas que indican el tipo de conversión.
    
 _lpMultiByteStr_
  
> a Puntero a la cadena de caracteres que se va a convertir.
    
 _cchMultiByte_
  
> a Tamaño, en bytes, de la cadena indicada por el parámetro _lpMultiByteStr_ . 
    
 _lpWideCharStr_
  
> [out] Opcional. Puntero a un búfer que recibe la cadena convertida.
    
 _cchWideChar_
  
> a Tamaño, en caracteres, del búfer indicado por _lpWideCharStr_.
    
## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres escritos en el búfer indicado por _lpWideCharStr_ si se realiza correctamente. 
  
## <a name="remarks"></a>Comentarios

Esta función ajusta la función **MultiByteToWideChar** . Para obtener más información, vea [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

