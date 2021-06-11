---
title: xlfUnregister (Formulario 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419908"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (Formulario 2)

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se puede llamar desde un comando DLL o XLL al que ha llamado Microsoft Excel. Esto equivale a llamar a **UNREGISTER** desde una Excel de macros XLM. 
  
**xlfUnregister** se puede llamar de dos formas: 
  
- Formulario 1: Anula el registro de un comando o función individual.
    
- Formulario 2: Descarga y desactiva un XLL.
    
Llamada en el formulario 2, esta función fuerza una DLL o un recurso de código a descargarse por completo. Anula el registro de todas las funciones de un ARCHIVO DLL, incluso si están actualmente en uso por otra macro, independientemente del recuento de uso. Esta función llama **a xlAutoClose** y, a continuación, anula el registro de todas las funciones de la DLL.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameters

_pxModuleText_ (**xltypeStr**)
  
El nombre de la DLL.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se realiza **correctamente, devuelve TRUE** (**xltypeBool**). Si no se realiza correctamente, **devuelve FALSE**.
  
## <a name="remarks"></a>Comentarios

> [!NOTE] 
> No llame a este formulario de la función desde la implementación del [xlAutoClose](xlautoclose.md) en un intento de anular el registro de todos los recursos del DLL con una llamada de función sencilla. Esto conduce a llamadas recursivas de **xlAutoClose y** un desbordamiento de pila. 
  
### <a name="remember-to-delete-names"></a>Recuerde eliminar nombres

Si especificó el argumento  _pxFunctionText_ en **xlfRegister**, al registrar las funciones y comandos del DLL, debe eliminar explícitamente los nombres llamando a **xlfSetName** para cada uno, omitiendo el segundo argumento para que la función ya no aparezca en el Asistente para funciones. Para obtener más información, consulta [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Vea también

- [xlfRegister (Formulario 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formulario 1)](xlfunregister-form-1.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

