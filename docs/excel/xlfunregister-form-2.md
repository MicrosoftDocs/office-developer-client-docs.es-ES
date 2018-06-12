---
title: xlfUnregister (formulario de 2)
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
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815750"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (formulario de 2)

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se pueden llamar desde un comando DLL o XLL que se ha llamado propio por Microsoft Excel. Esto equivale a llamar al **Cancelar el registro** de una hoja de macros XLM de Excel. 
  
**xlfUnregister** se puede llamar de dos formas: 
  
- Formulario 1: Anula el registro de un comando individual o una función.
    
- Formulario 2: Descarga y desactiva un XLL.
    
Llama a en el formulario 2, esta función obliga a un archivo DLL o recurso de código para ser descargado completamente. Anula el registro de todas las funciones en una DLL, incluso si están actualmente en uso por otra macro, independientemente de qué el recuento de uso. Esta función llama **xlAutoClose**y, a continuación, anula el registro de todas las funciones en el archivo DLL.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Sintaxis

_pxModuleText_ (**xltypeStr**)
  
El nombre del archivo DLL.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

Si se realiza correctamente, devuelve **TRUE** (**xltypeBool**). Si no lo consigue, devuelve **FALSE**.
  
## <a name="remarks"></a>Notas

> [!NOTE] 
> No llame a esta forma de la función de la implementación de la [xlAutoClose](xlautoclose.md) en un intento de anular el registro de todos los recursos del archivo DLL con la llamada a una función simple de. Esto tiene las siguientes consecuencias llamada recursiva de **xlAutoClose** y un desbordamiento de pila. 
  
### <a name="remember-to-delete-names"></a>No olvide eliminar nombres

Si especifica el argumento _pxFunctionText_ para **xlfRegister**, cuando se registra la DLL funciones y comandos, se deben eliminar explícitamente los nombres mediante una llamada a **xlfSetName** para cada uno de ellos se omite el segundo argumento para que el función ya no aparece en el Asistente para la función. Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Ver también

- [xlfRegister (formulario 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (formulario 1)](xlfunregister-form-1.md)
- [Funciones de API XLM esenciales y útil C](essential-and-useful-c-api-xlm-functions.md)

