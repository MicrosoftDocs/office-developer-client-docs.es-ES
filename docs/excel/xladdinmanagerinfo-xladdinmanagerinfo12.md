---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- función xladdinmanagerinfo [Excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304000"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llamado por Microsoft Excel cuando se invoca el administrador de complementos por primera vez en una sesión de Excel. Esta función se usa para proporcionar al administrador de complementos información sobre el complemento.
  
Excel 2007 y versiones posteriores llaman a **xlAddInManagerInfo12** en prioridad a **xlAddInManagerInfo** si se exportan por el XLL. La función **xlAddInManagerInfo12** debe funcionar de la misma manera que **xlAddInManagerInfo** para evitar diferencias específicas de la versión en el comportamiento del XLL. Excel espera que **xlAddInManagerInfo12** devuelva un tipo de datos **XLOPER12** , mientras que **xlAddInManagerInfo** debe devolver un **XLOPER**.
  
Las versiones de Excel anteriores a Excel 2007 no llaman a la función **xlAddInManagerInfo12** , ya que no son compatibles con **XLOPER12**.
  
Excel no requiere un XLL que implemente y exporte cualquiera de estas funciones.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parameters

 _pxAction:_ Un puntero a un **XLOPER o XLOPER12** numérico (**xltypeInt** o **xltypeNum**).
  
La información que Excel solicita.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si _pxAction_ es o se puede convertir en el número 1, la implementación de esta función debe devolver una cadena que contenga información sobre el complemento, normalmente su nombre y quizá un número de versión. De lo contrario, debe devolver #VALUE!. 
  
Si no devuelve una cadena, Excel intenta convertir el valor devuelto en una cadena.
  
## <a name="remarks"></a>Comentarios

Si la cadena devuelta apunta a un búfer asignado dinámicamente, debe asegurarse de que este búfer se libere finalmente. Si la cadena fue asignada por Excel, puede hacerlo estableciendo **xlbitXLFree**. Si la cadena fue asignada por la DLL, para ello, se establece **xlbitDLLFree**y también se debe implementar en [xlAutoFree](xlautofree-xlautofree12.md) (si se va a devolver un **XLOPER**) o **xlAutoFree12** (si se va a devolver un **XLOPER12**).
  
## <a name="example"></a>Ejemplo

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a>Vea también



[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

