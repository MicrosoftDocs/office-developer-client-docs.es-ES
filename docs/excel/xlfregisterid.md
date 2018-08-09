---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid (función) [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815740"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se pueden llamar desde un archivo DLL que se ha llamado propio por Microsoft Excel. Si una función ya está registrada, devuelve el identificador de registro existente para esa función sin volver a registrarlo. Si una función aún no esté registrada, registra y devuelve el identificador del registro resultante.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parámetros

_pxModuleText_ (**xltypeStr**)
  
El nombre del archivo DLL que contiene la función.
  
_pxProcedure_ (**xltypeStr** o **xltypeNum**)
  
Si hay una cadena, el nombre de la función que se llama. Si un número, el ordinal exportar el número de la función que se llama. Para mayor claridad y solidez, use siempre el formato de cadena.
  
_pxTypeText_ (**xltypeStr**)
  
Una cadena opcional que especifica los tipos de todos los argumentos a la función y el tipo del valor devuelto de la función. Para obtener más información, vea la sección "Comentarios". Este argumento puede omitirse para un archivo DLL independiente (XLL) definición **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el identificador de registro de la función (**xltypeNum**), que se puede utilizar en las llamadas subsiguientes a **xlfUnregister**.
  
## <a name="remarks"></a>Comentarios

Esta función es útil cuando no desea preocuparse de mantener un identificador de registro, pero necesita una más adelante para anular el registro. También es útil para asignar a los menús, herramientas y los botones cuando la función que desea asignar está en un archivo DLL.
  
Cuando una función DLL o XLL se ha registrado con un argumento válido _pxFunctionText_ tener ha proporcionado para **xlfRegister**, su identificador de registro también puede obtenerse pasando el _pxFunctionText_ a la función **xlfEvaluate**.
  
## <a name="see-also"></a>Vea también

- [REGISTRAR](xlfregister-form-1.md)
- [ANULAR EL REGISTRO](xlfunregister-form-1.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

