---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301620"
---
# <a name="pingsession"></a>PingSession

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comprueba si una sesión es válida. Normalmente, se llama a esta función cuando Excel necesita determinar si un identificador de sesión devuelto anteriormente todavía está activo y se puede usar.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Parameters

_SessionID_
  
> IDENTIFICADOR de la sesión a la que se va a hacer ping. Este valor debe coincidir con un identificador devuelto por una llamada anterior a [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si el argumento _SessionID_ es válido; de lo contrario **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Vea también

- [OpenSession](opensession.md)
- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

