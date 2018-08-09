---
title: xlfRegister (Formulario 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- función xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815727"
---
# <a name="xlfregister-form-2"></a>xlfRegister (Formulario 2)

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se pueden llamar desde un comando DLL o XLL que se ha llamado propio por Microsoft Excel. Esto equivale a llamar al **registrar** desde una hoja de macros XLM de Excel. 
  
Puede llamar a la función **xlfRegister** de dos formas: 
  
- [xlfRegister (formulario 1)](xlfregister-form-1.md): registra un comando individual o una función.
    
- xlfRegister (formulario 2): cargas y se activa un XLL.
    
Llama a en el formulario 2, esta función sólo se puede usar para cargar y activar un XLL que contiene un procedimiento [xlAutoOpen](xlautoopen.md) . 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parámetros

 _pxModuleText_ (**xltypeStr**)
  
El nombre de la DLL que se va a cargar y activar.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se realiza correctamente, se devuelve el nombre del archivo DLL (**xltypeStr**). ¡En caso contrario, devuelve #VALUE! error.
  
## <a name="see-also"></a>Vea también



[Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

