---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- función xlfregisterid [Excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303881"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se puede llamar desde una DLL que ha sido llamada por Microsoft Excel. Si una función ya está registrada, devuelve el identificador de registro existente para esa función sin volver a registrarla. Si una función todavía no está registrada, se registra y se devuelve el identificador de registro resultante.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parameters

_pxModuleText_ (**xltypeStr**)
  
Nombre del archivo DLL que contiene la función.
  
_pxProcedure_ (**xltypeStr** o **xltypeNum**)
  
Si es una cadena, el nombre de la función a la que se llama. Si es un número, el número de exportación ordinal de la función que se va a llamar. Para mayor claridad y solidez, use siempre el formato de cadena.
  
_pxTypeText_ (**xltypeStr**)
  
Una cadena opcional que especifica los tipos de todos los argumentos de la función y el tipo de valor devuelto de la función. Si desea más información, vea la sección "Comentarios". Este argumento puede omitirse para una DLL independiente (XLL) que defina **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el identificador de registro de la función (**xltypeNum**), que se puede usar en llamadas posteriores a **xlfUnregister**.
  
## <a name="remarks"></a>Comentarios

Esta función es útil cuando no desea preocuparse por mantener un identificador de registro, pero necesita uno más adelante para anular el registro. También es útil para asignar menús, herramientas y botones cuando la función que desea asignar está en una DLL.
  
Cuando se ha registrado una función DLL o XLL con un argumento _pxFunctionText_ válido que se ha proporcionado a **xlfRegister**, también se puede obtener su identificador de registro pasando el _pxFunctionText_ a la función **xlfEvaluate**.
  
## <a name="see-also"></a>Vea también

- [Registre](xlfregister-form-1.md)
- [ANULAR el registro](xlfunregister-form-1.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

