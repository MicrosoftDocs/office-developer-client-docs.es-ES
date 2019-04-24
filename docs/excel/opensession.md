---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301634"
---
# <a name="opensession"></a>OpenSession

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Crea una sesión en la que se pueden ejecutar funciones definidas por el usuario.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Parameters

_Params_
  
> Puntero a una cadena uniCODE delimitada por punto y coma de los parámetros de la sesión. Excel no utiliza este argumento.
    
## <a name="return-value"></a>Valor devuelto

Un identificador de sesión que se va a usar en otras llamadas al conector de clúster, si la sesión se ha creado correctamente; de lo contrario **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Vea también

- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

