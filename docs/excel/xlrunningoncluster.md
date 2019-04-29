---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418291"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve un valor que indica si la función definida por el usuario se está ejecutando en un clúster. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameters

Esta función no tiene argumentos.
  
## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta en un proceso de Excel, devuelve 0 en un **XLOPER12** de tipo **xlTypeInt**. Si la función se ejecuta en un clúster, el tipo de valor devuelto y el valor se determinan mediante el proveedor del conector del clúster.
  
## <a name="requirements"></a>Requisitos

Esta función se define en el archivo de encabezado xlcall. h.
  
## <a name="see-also"></a>Ver también

- [Funciones seguras para clústeres](cluster-safe-functions.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

