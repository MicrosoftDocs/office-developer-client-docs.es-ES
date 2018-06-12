---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815705"
---
# <a name="pingsession"></a>PingSession

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comprueba si una sesión es válida. Normalmente, se llama a esta función cuando Excel necesita para determinar si un identificador de sesión devueltos anteriormente todavía está activo y se puede usar.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Sintaxis

_SessionID_
  
> El identificador de la sesión para hacer ping. Este valor debe coincidir con un identificador devuelto por una llamada anterior a [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si el argumento de _SessionId_ es válido; en caso contrario, **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Ver también

- [OpenSession](opensession.md)
- [Funciones de conector de clúster de Excel](excel-cluster-connector-functions.md)

