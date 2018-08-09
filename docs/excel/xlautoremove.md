---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlautoremove (función) [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815728"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llamado por Microsoft Excel cada vez que el usuario desactiva el XLL durante una sesión de Excel mediante el uso del administrador. Esta función no se llama cuando se cierra una sesión de Excel, normalmente o de forma anómala, con el complemento instalado.
  
Esta función puede usarse para mostrar un cuadro de diálogo personalizado que indica al usuario que el complemento se ha desactivado, o para leer o escribir en el registro, por ejemplo.
  
Excel no requiere un XLL implementar y exportar a esta función. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La implementación de esta función debe devolver 1 (**int**).
  
## <a name="remarks"></a>Comentarios

Utilice esta función si necesita su XLL para llevar a cabo cualquier tarea cuando se elimina mediante el Administrador de complementos.
  
## <a name="example"></a>Ejemplo

Ver los archivos `\SAMPLES\EXAMPLE\EXAMPLE.C` y `\SAMPLES\GENERIC\GENERIC.C` para las implementaciones de ejemplo de esta función. El código siguiente es de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a>Vea también



[xlAutoAdd](xlautoadd.md)


[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

