---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- función xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425480"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se llama Microsoft Excel cuando el usuario desactiva el XLL durante una sesión Excel mediante el administrador de Add-In usuario. No se llama a esta función cuando una sesión de Excel se cierra, de forma normal o excepcional, con el complemento instalado.
  
Esta función se puede usar para mostrar un cuadro de diálogo personalizado que le diga al usuario que el complemento se ha desactivado, o para leer o escribir en el Registro, por ejemplo.
  
Excel requiere un XLL para implementar y exportar esta función. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La implementación de esta función debe devolver 1 (**int**).
  
## <a name="remarks"></a>Comentarios

Use esta función si el XLL necesita completar cualquier tarea cuando el Administrador de Add-In elimina.
  
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

