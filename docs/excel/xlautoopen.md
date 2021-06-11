---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- función xlautoopen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406650"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de devolución de llamada que todos los XLL válidos deben implementar y exportar. La **función xlAutoOpen** es el lugar recomendado desde el que registrar funciones y comandos XLL, inicializar estructuras de datos, personalizar la interfaz de usuario, y así sucesivamente. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La implementación de esta función debe devolver 1 (**int**).
  
## <a name="remarks"></a>Comentarios

Microsoft Excel llamadas **xlAutoOpen** cada vez que se activa XLL. El XLL se activa en las siguientes situaciones: 
  
- Al principio de una sesión de Excel si estaba activa en la última sesión Excel sesión que finalizaba normalmente.
    
- Si se carga durante una Excel sesión.
    
- Un XLL se puede cargar de varias maneras:
    
- Al elegir **Abrir en** el **menú** Archivo (donde la versión de Excel admite este método de carga de XLLs). 
    
- Usando el Administrador de complementos.
    
- Desde otro XLL que llama [a xlfRegister](xlfregister-form-1.md) con el nombre de este DLL como único argumento. 
    
- Desde una hoja de macros XLM que llama [a REGISTER](xlfregister-form-1.md) con el nombre de esta DLL como único argumento. 
    
- Si el complemento se desactiva y se reactiva durante una sesión Excel, se llama a esta función en la reactivación.
    
### <a name="example"></a>Ejemplo

Vea los archivos  `SAMPLES\EXAMPLE\EXAMPLE.C` y , y por ejemplo las  `SAMPLES\GENERIC\GENERIC.C` implementaciones de esta función.
  
## <a name="see-also"></a>Vea también



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

