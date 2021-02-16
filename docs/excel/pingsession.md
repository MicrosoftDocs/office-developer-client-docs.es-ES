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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408365"
---
# <a name="pingsession"></a>PingSession

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comprueba si una sesión es válida. Normalmente se llama a esta función cuando Excel necesita determinar si un identificador de sesión devuelto anteriormente sigue activo y se puede usar.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Parámetros

_SessionID_
  
> Identificador de la sesión que se debe hacer ping. Este valor debe coincidir con un identificador devuelto por una llamada anterior a [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si el  _argumento SessionId_ es válido; de **lo contrario xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Consulte también

- [OpenSession](opensession.md)
- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

