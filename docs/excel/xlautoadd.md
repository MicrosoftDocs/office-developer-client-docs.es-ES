---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd (función) [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815710"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Agregados por Microsoft Excel cada vez que el usuario activa el XLL durante una sesión de Excel mediante el uso del administrador. Esta función no se llama cuando Excel se inicia y carga un complemento preinstalado.
  
Esta función puede utilizarse para mostrar un cuadro de diálogo personalizado que indica al usuario que el complemento se ha activado, o para leer o escribir en el registro o comprobar la información de licencias, por ejemplo.
  
Excel no requiere un XLL implementar y exportar a esta función.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La implementación de esta función debe devolver 1. (**int**).
  
## <a name="remarks"></a>Comentarios

Utilice esta función si no hay nada que su XLL necesita hacer cuando se agrega por el Administrador de complementos.
  
## <a name="example"></a>Ejemplo

Vea `\SAMPLES\EXAMPLE\EXAMPLE.C` y `\SAMPLES\GENERIC\GENERIC.C` por ejemplo las implementaciones de esta función. El código siguiente es de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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

