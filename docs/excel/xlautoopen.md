---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- función xlAutoOpen [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310293"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de devolución de llamada que debe implementar y exportar cada XLL válido. La función **xlAutoOpen** es el lugar recomendado desde donde se registran las funciones y los comandos XLL, inicializan estructuras de datos, personalizan la interfaz de usuario, etc. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La implementación de esta función debe devolver 1 (**int**).
  
## <a name="remarks"></a>Comentarios

Microsoft Excel llama a **xlAutoOpen** siempre que se activa el XLL. El XLL se activa en las siguientes situaciones: 
  
- Al inicio de una sesión de Excel si estaba activa en la última sesión de Excel que finalizó con normalidad.
    
- Si se carga durante una sesión de Excel.
    
- Un XLL se puede cargar de varias maneras:
    
- Eligiendo **abrir** en el menú **archivo** (donde la versión de Excel admite este método de carga de XLL). 
    
- Usando el Administrador de complementos.
    
- De otro XLL que llama a [xlfRegister](xlfregister-form-1.md) con el nombre de este dll como único argumento. 
    
- Desde una hoja de macros XLM que llama a [Register](xlfregister-form-1.md) con el nombre de este archivo dll como único argumento. 
    
- Si el complemento se desactiva y se reactiva durante una sesión de Excel, se llama a esta función en la reactivación.
    
### <a name="example"></a>Ejemplo

Vea los archivos `SAMPLES\EXAMPLE\EXAMPLE.C` y `SAMPLES\GENERIC\GENERIC.C`, por ejemplo, las implementaciones de esta función.
  
## <a name="see-also"></a>Vea también



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

