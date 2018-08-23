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
ms.openlocfilehash: 66e8c3b61caac6fb8d8b57d74ade6fa8aac3a9dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571712"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Es similar a **MultiByteToWideChar**, que se asigna una cadena de caracteres en una cadena de UTF-16 (carácter ancho). La cadena de caracteres no está necesariamente desde un carácter de varios bytes establecida.
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>Parámetros

 _uCodePage_
  
> [entrada] Página de códigos a utilizar para realizar la conversión.
    
 _dwFlags_
  
> [entrada] Marcas que indica el tipo de conversión.
    
 _lpMultiByteStr_
  
> [entrada] Puntero a la cadena de caracteres para convertir.
    
 _cchMultiByte_
  
> [entrada] Tamaño, en bytes, de la cadena indicada por el parámetro _lpMultiByteStr_ . 
    
 _lpWideCharStr_
  
> [out] Opcional. Puntero a un búfer que recibe la cadena convertida.
    
 _cchWideChar_
  
> [entrada] Tamaño, en caracteres, del búfer indicado por _lpWideCharStr_.
    
## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres escritos en el búfer indicado por _lpWideCharStr_ si se realiza correctamente. 
  
## <a name="remarks"></a>Comentarios

Esta función ajusta la función **MultiByteToWideChar** . Para obtener más información, vea [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).
  

