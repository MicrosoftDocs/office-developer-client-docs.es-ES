---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- función fshowdialog [Excel 2007]
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
  
Comando de ejemplo definido por el usuario que carga y muestra un cuadro de diálogo de Windows nativo de ejemplo. Cuando se carga GENERIC. XLL, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parameters

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función devuelve un entero cero para indicar que la operación se completó correctamente
  
## <a name="remarks"></a>Comentarios

Los pasos para mostrar el cuadro de diálogo de Windows nativo son los siguientes:
  
1. Obtener el identificador principal de Windows de Microsoft Excel mediante **GetHwnd**.
    
2. Enlace la ventana principal de Excel mediante **HookExcelWindow**.
    
3. Mostrar el cuadro de diálogo mediante **DialogBox**.
    
4. Desenlaza la ventana principal de Excel mediante **UnhookExcelWindow**.
    
### <a name="example"></a>Ejemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función. 
  
## <a name="see-also"></a>Ver también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

