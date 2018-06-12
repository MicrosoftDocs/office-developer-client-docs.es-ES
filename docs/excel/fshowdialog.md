---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fshowdialog (función) [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815643"
---
# <a name="fshowdialog"></a>fShowDialog

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Definidas por el usuario comando de ejemplo que se carga y se muestra un cuadro de diálogo de Windows nativo de ejemplo. Cuando se carga GENERIC.xll, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Sintaxis

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

El entero devuelto de función cero para indicar la finalización correcta
  
## <a name="remarks"></a>Notas

Los pasos para mostrar el cuadro de diálogo de Windows nativo son los siguientes:
  
1. Obtener el identificador de Windows principal de Microsoft Excel utilizando **GetHwnd**.
    
2. La ventana principal de Excel con **HookExcelWindow**de enlace.
    
3. Mostrar el cuadro de diálogo con **DialogBox**.
    
4. Eliminar enlaces de la ventana principal de Excel mediante **UnhookExcelWindow**.
    
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Ver también



[Funciones en el archivo DLL genérica](functions-in-the-generic-dll.md)

