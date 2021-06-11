---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- función xlfregisterid [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420062"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se puede llamar desde un ARCHIVO DLL al que ha llamado Microsoft Excel. Si una función ya está registrada, devuelve el identificador de registro existente para esa función sin volver a registrarla. Si una función aún no está registrada, la registra y devuelve el identificador de registro resultante.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parameters

_pxModuleText_ (**xltypeStr**)
  
Nombre de la DLL que contiene la función.
  
_pxProcedure_ (**xltypeStr** o **xltypeNum**)
  
Si es una cadena, el nombre de la función a la que se llamará. Si es un número, el número de exportación ordinal de la función a la que se debe llamar. Para mayor claridad y solidez, use siempre el formulario de cadena.
  
_pxTypeText_ (**xltypeStr**)
  
Una cadena opcional que especifica los tipos de todos los argumentos de la función y el tipo del valor devuelto de la función. Si desea más información, vea la sección "Comentarios". Este argumento se puede omitir para un DLL independiente (XLL) que define **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el identificador de registro de la función (**xltypeNum**), que se puede usar en llamadas posteriores a **xlfUnregister**.
  
## <a name="remarks"></a>Comentarios

Esta función es útil cuando no desea preocuparse por mantener un identificador de registro, pero necesita uno más adelante para anular el registro. También resulta útil para asignar menús, herramientas y botones cuando la función que desea asignar está en un ARCHIVO DLL.
  
Cuando se ha registrado una función DLL o XLL con un argumento  _pxFunctionText_ válido que se ha proporcionado a **xlfRegister,** su identificador de registro también se puede obtener pasando  _pxFunctionText_ a la función **xlfEvaluate**.
  
## <a name="see-also"></a>Vea también

- [REGISTER](xlfregister-form-1.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

