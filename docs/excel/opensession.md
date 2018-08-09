---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815692"
---
# <a name="opensession"></a>OpenSession

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Crea una sesión en el que se pueden ejecutar funciones definidas por el usuario.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Parámetros

_Params_
  
> Un puntero a la cadena UNICODE delimitada por punto y coma de los parámetros de la sesión. Excel no utiliza este argumento.
    
## <a name="return-value"></a>Valor devuelto

Un identificador de sesión para usar en otras llamadas para el conector de clúster, si la sesión se ha creado correctamente; en caso contrario, **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Vea también

- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

