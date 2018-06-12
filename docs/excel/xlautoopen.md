---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- función xlAutoOpen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815711"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de devolución de llamada que se debe implementar y exportada por cada XLL válido. La función **xlAutoOpen** es el lugar recomendado de dónde los comandos y las funciones XLL de registrar, inicializar las estructuras de datos, personalizar la interfaz de usuario y así sucesivamente. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Sintaxis

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

La implementación de esta función debe devolver 1 (**int**).
  
## <a name="remarks"></a>Notas

Microsoft Excel llama **xlAutoOpen** cada vez que se activa el XLL. El XLL está activado en las situaciones siguientes: 
  
- En el inicio de una sesión de Excel si estaba activo en la última sesión de Excel que finalizó normalmente.
    
- Si se cargan durante una sesión de Excel.
    
- Un XLL se puede cargar de varias maneras:
    
- Si elige **Abrir** en el menú **archivo** (donde la versión de Excel es compatible con este método de carga de los XLL). 
    
- Con el Administrador de complementos.
    
- Desde otro XLL que llama a [xlfRegister](xlfregister-form-1.md) con el nombre de este archivo DLL como el único argumento. 
    
- Desde una hoja de macros XLM que llama a [registrar](xlfregister-form-1.md) con el nombre de este archivo DLL como el único argumento. 
    
- Si el complemento está desactivado y reactiva durante una sesión de Excel, se llama a esta función en la reactivación.
    
### <a name="example"></a>Ejemplo

Consulte los archivos `SAMPLES\EXAMPLE\EXAMPLE.C` y `SAMPLES\GENERIC\GENERIC.C`y por ejemplo las implementaciones de esta función.
  
## <a name="see-also"></a>Ver también



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Administrador de complementos y funciones de la interfaz XLL](add-in-manager-and-xll-interface-functions.md)

