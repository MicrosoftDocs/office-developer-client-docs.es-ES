---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- función initframework [Excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420758"
---
# <a name="initframework"></a>InitFramework

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de marcos que inicializa la biblioteca de .NET Framework, que simplemente inicializa las estructuras de datos de memoria**XLOPER12** de **XLOPER**/ temporales, liberando cualquier memoria que ya se haya asignado. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="return-value"></a>Valor devuelto

Esta función no devuelve un valor.
  
## <a name="example"></a>Ejemplo

En este ejemplo, se usa la función **InitFramework** para liberar toda la memoria temporal. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

