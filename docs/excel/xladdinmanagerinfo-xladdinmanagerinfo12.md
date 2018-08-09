---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- xladdinmanagerinfo (función) [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815704"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llamado por Microsoft Excel cuando se invoca el Administrador de complementos por primera vez en una sesión de Excel. Esta función se usa para proporcionar información sobre el complemento del administrador.
  
Excel 2007 y versiones posteriores de llamadas **xlAddInManagerInfo12** preferentemente **xlAddInManagerInfo** si exportada por el XLL. La función **xlAddInManagerInfo12** debería funcionar de la misma manera como **xlAddInManagerInfo** para evitar las diferencias específicas de la versión en el comportamiento de los XLL. Excel espera **xlAddInManagerInfo12** para devolver un tipo de datos **XLOPER12** , mientras que **xlAddInManagerInfo** debe devolver un **XLOPER**.
  
No se llama a la función **xlAddInManagerInfo12** por las versiones anteriores a Excel 2007, ya que estos no admiten la **XLOPER12**.
  
Excel no requiere un XLL implementar y exportar a cualquiera de estas funciones.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parámetros

 _pxAction:_ Un puntero a un numérico **XLOPER y XLOPER12** (**xltypeInt** o **xltypeNum**).
  
La información que se solicita Excel.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si _pxAction_ es, o se pueda convertir a, el número 1, a continuación, la implementación de esta función debe devolver una cadena que contiene información sobre el complemento, normalmente su nombre y, posiblemente, un número de versión. En caso contrario, se debe devolver #VALUE!. 
  
Si no se devuelve una cadena, Excel intenta convertir el valor devuelto en una cadena.
  
## <a name="remarks"></a>Comentarios

Si la cadena devuelta apunta al búfer asignado dinámicamente, debe asegurarse de que este búfer se libera finalmente. Si la cadena asignada por Excel, ello estableciendo **xlbitXLFree**. Si la cadena se ha asignado por el archivo DLL, para ello, configuración **xlbitDLLFree**, y también se debe implementar en [xlAutoFree](xlautofree-xlautofree12.md) (si va a devolver un **XLOPER**) o **xlAutoFree12** (si se va a devolver un **XLOPER12**).
  
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

