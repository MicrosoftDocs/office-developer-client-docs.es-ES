---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- Función xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407798"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llamado por Microsoft Excel cuando se invoca el Administrador de complementos por primera vez en una sesión de Excel. Esta función se usa para proporcionar al administrador de Add-In información sobre el complemento.
  
Excel 2007 y versiones posteriores llaman a **xlAddInManagerInfo12** en preferencia a **xlAddInManagerInfo** si lo exporta el XLL. La **función xlAddInManagerInfo12** debe funcionar del mismo modo que **xlAddInManagerInfo** para evitar diferencias específicas de la versión en el comportamiento del XLL. Excel espera **que xlAddInManagerInfo12** devuelva un tipo de datos **XLOPER12,** mientras que **xlAddInManagerInfo** debe devolver **un XLOPER**.
  
Las versiones de Excel anteriores a Excel 2007 no llaman a la función **xlAddInManagerInfo12,** ya que no son compatibles con **XLOPER12**.
  
Excel no requiere un XLL para implementar y exportar ninguna de estas funciones.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parámetros

 _pxAction:_ Puntero a un **XLOPER/XLOPER12** numérico (**xltypeInt** o **xltypeNum**).
  
La información que Excel está solicitando.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si  _pxAction_ es o se puede convertir en el número 1, la implementación de esta función debe devolver una cadena que contenga cierta información sobre el complemento, normalmente su nombre y quizás un número de versión. De lo contrario, debería devolver #VALUE!. 
  
Si no devuelve una cadena, Excel intenta convertir el valor devuelto en una cadena.
  
## <a name="remarks"></a>Comentarios

Si la cadena devuelta apunta al búfer asignado dinámicamente, debes asegurarte de que este búfer se libera finalmente. Si Excel asignó la cadena, debe establecer **xlbitXLFree** para hacerlo. Si la dll asignó la cadena, debe establecer **xlbitDLLFree** y también debe implementarla en [xlAutoFree](xlautofree-xlautofree12.md) (si devuelve un **XLOPER)** o **xlAutoFree12** (si devuelve un **XLOPER12**).
  
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

