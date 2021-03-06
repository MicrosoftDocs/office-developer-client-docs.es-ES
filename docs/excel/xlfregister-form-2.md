---
title: xlfRegister (Formulario 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- función xlfregister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416044"
---
# <a name="xlfregister-form-2"></a>xlfRegister (Formulario 2)

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se puede llamar desde un comando DLL o XLL al que ha llamado Microsoft Excel. Esto equivale a llamar a **REGISTER** desde una Excel de macros XLM. 
  
Se puede llamar a la función **xlfRegister** en dos formularios: 
  
- [xlfRegister (formulario 1):](xlfregister-form-1.md)registra un comando o función individual.
    
- xlfRegister (formulario 2): carga y activa un XLL.
    
Llamada en el formulario 2, esta función solo se puede usar para cargar y activar un XLL que contenga un [procedimiento xlAutoOpen.](xlautoopen.md) 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameters

 _pxModuleText_ (**xltypeStr**)
  
Nombre de la DLL que se va a cargar y activar.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se realiza correctamente, devuelve el nombre de la DLL (**xltypeStr**). De lo contrario, devuelve un #VALUE! error.
  
## <a name="see-also"></a>Vea también



[Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

