---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422540"
---
# <a name="closesession"></a>CloseSession

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Finaliza una sesión con un clúster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Parameters

_SessionId_
  
> El identificador de la sesión que se cerrará. Este valor debe coincidir con el valor devuelto por [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si la sesión se cerró; **xlHpcRetInvalidSessionId** si el  _argumento SessionId_ no es válido; **xlHpcRetCallFailed en** otros errores. 
  
## <a name="see-also"></a>Vea también

- [OpenSession](opensession.md)
- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

