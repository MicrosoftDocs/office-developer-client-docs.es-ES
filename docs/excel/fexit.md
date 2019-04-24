---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- función fexit [Excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310860"
---
# <a name="fexit"></a>fExit

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comando definido por el usuario de ejemplo que descarga GENERIC. XLL. Cuando se carga GENERIC. XLL, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parameters

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función siempre devuelve 1.
  
## <a name="remarks"></a>Comentarios

Se trata de una rutina iniciada por el usuario para salir de GENERIC. XLL debe `UNREGISTER("GENERIC.XLL")` evitar llamar simplemente en esta función. Esto forzaría la anulación del registro de todas las funciones de esta DLL, incluso si están registradas en algún otro lugar. En su lugar, anule el registro de las funciones de una en una. 
  
### <a name="example"></a>Ejemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

