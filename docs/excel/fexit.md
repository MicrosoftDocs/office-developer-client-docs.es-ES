---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- función fexit [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429918"
---
# <a name="fexit"></a>fExit

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Ejemplo de comando definido por el usuario que descarga GENERIC.xll. Cuando se carga GENERIC.xll, crea un menú definido por el usuario, Generic, a través del cual se tiene acceso a este comando. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parámetros

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función siempre devuelve 1.
  
## <a name="remarks"></a>Comentarios

Se trata de una rutina iniciada por el usuario para salir de GENERIC.xll. Debe evitar simplemente llamar  `UNREGISTER("GENERIC.XLL")` a esta función. Esto anularía por la fuerza el registro de todas las funciones de esta DLL, incluso si están registradas en otro lugar. En su lugar, anula el registro de las funciones de una en una. 
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Consulte también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

