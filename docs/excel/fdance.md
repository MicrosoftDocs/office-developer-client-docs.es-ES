---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- función fdance [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311042"
---
# <a name="fdance"></a>fDance

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comando definido por el usuario de ejemplo que cambia las celdas seleccionadas en la hoja de cálculo activa hasta que el usuario presiona la **tecla ESC**. Cuando se carga GENERIC. XLL, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parameters

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función siempre devuelve 1.
  
## <a name="remarks"></a>Comentarios

Este es un ejemplo de una operación larga. Llama a la función [xlAbort](xlabort.md) de vez en cuando. Esto produce el procesador (ayudando con la multitarea cooperativa) y comprueba si el usuario ha presionado **ESC** para cancelar la operación. Si es así, ofrece al usuario la posibilidad de cancelar la anulación. 
  
### <a name="example"></a>Ejemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

