---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- función fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433594"
---
# <a name="fshowdialog"></a>fShowDialog

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Ejemplo de comando definido por el usuario que carga y muestra un cuadro de diálogo nativo Windows ejemplo. Cuando se carga GENERIC.xll, se crea un menú definido por el usuario, Generic, a través del cual se tiene acceso a este comando.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parameters

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función devuelve cero entero para indicar que se ha completado correctamente
  
## <a name="remarks"></a>Comentarios

Los pasos para mostrar el cuadro Windows de diálogo nativo son los siguientes:
  
1. Obtener el Microsoft Excel principal Windows con **GetHwnd**.
    
2. Enlazar la Excel principal mediante **HookExcelWindow**.
    
3. Mostrar el cuadro de diálogo mediante **DialogBox**.
    
4. Desenganche la Excel principal con **UnhookExcelWindow**.
    
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

