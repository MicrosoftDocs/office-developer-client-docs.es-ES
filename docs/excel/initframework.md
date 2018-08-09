---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- initframework (función) [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815633"
---
# <a name="initframework"></a>InitFramework

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de la biblioteca de Framework que inicializa la biblioteca Framework, que simplemente inicializa el temporal **XLOPER**/ las estructuras de datos de memoria**XLOPER12** , liberar cualquier memoria que ya ha sido asignada. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="return-value"></a>Valor devuelto

Esta función no devuelve un valor.
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa la función de **InitFramework** para liberar toda la memoria temporal. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

