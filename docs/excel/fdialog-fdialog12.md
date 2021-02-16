---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- función fdialog [excel 2007],función fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431529"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Ejemplo de comando definido por el usuario que muestra cómo crear una UDD de Microsoft Excel (cuadro de diálogo definido por el usuario) dentro de una DLL mediante las capacidades de cuadro de diálogo en la API de C. Cuando se carga GENERIC.xll, crea un menú definido por el usuario, Generic, a través del cual se tiene acceso a este comando.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Parámetros

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función siempre devuelve 1.
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Consulte también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

