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
- función fDialog [excel 2007], fDialog12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815629"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usuario definido por el comando de ejemplo que se muestra cómo crear un UDD de Microsoft Excel (cuadro de diálogo definidas por el usuario) dentro de un archivo DLL mediante el uso de las capacidades de cuadro de diálogo de la API de C. Cuando se carga GENERIC.xll, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Sintaxis

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

La función siempre devuelve 1.
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Ver también



[Funciones en el archivo DLL genérica](functions-in-the-generic-dll.md)

