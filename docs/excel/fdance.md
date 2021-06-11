---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- función fdance [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409051"
---
# <a name="fdance"></a>fDance

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Ejemplo de comando definido por el usuario que cambia las celdas seleccionadas de la hoja de cálculo activa hasta que el usuario presiona **ESC**. Cuando se carga GENERIC.xll, se crea un menú definido por el usuario, Generic, a través del cual se tiene acceso a este comando.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parameters

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función siempre devuelve 1.
  
## <a name="remarks"></a>Comentarios

Este es un ejemplo de una operación larga. Llama a la función [xlAbort ocasionalmente.](xlabort.md) Esto genera el procesador (lo que ayuda con la multitarea cooperativa) y comprueba si el usuario ha presionado **ESC** para cancelar la operación. Si es así, ofrece al usuario la oportunidad de cancelar la anulación. 
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

