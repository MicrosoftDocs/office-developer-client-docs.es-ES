---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- función xlautoadd [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413762"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se agrega mediante Microsoft Excel cuando el usuario activa el XLL durante una sesión Excel mediante el administrador de Add-In usuario. No se llama a esta función Excel se inicia y se carga un complemento preinstalado.
  
Esta función se puede usar para mostrar un cuadro de diálogo personalizado que indica al usuario que el complemento se ha activado, leer o escribir en el Registro, o comprobar la información de licencias, por ejemplo.
  
Excel requiere un XLL para implementar y exportar esta función.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La implementación de esta función debe devolver 1. (**int**).
  
## <a name="remarks"></a>Comentarios

Use esta función si hay algo que el XLL necesita hacer cuando la agrega el administrador de Add-In.
  
## <a name="example"></a>Ejemplo

Vea  `\SAMPLES\EXAMPLE\EXAMPLE.C`  `\SAMPLES\GENERIC\GENERIC.C` y, por ejemplo, implementaciones de esta función. El código siguiente es de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a>Vea también



[xlAutoRemove](xlautoremove.md)


[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

