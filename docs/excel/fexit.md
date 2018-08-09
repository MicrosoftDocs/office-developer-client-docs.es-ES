---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit (función) [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815624"
---
# <a name="fexit"></a>fExit

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usuario definido por el comando de ejemplo que descarga GENERIC.xll. Cuando se carga GENERIC.xll, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parámetros

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función siempre devuelve 1.
  
## <a name="remarks"></a>Comentarios

Ésta es una rutina iniciadas por el usuario para salir GENERIC.xll debe evitar simplemente al llamar a `UNREGISTER("GENERIC.XLL")` en esta función. Esto haría forzosamente anular el registro de todas las funciones de este archivo DLL, incluso si están registrados en algún lugar ningún otro punto. En su lugar, anular el registro de las funciones de uno a la vez. 
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones de la DLL genérica](functions-in-the-generic-dll.md)

