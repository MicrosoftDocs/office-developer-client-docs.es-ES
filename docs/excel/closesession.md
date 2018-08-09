---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815529"
---
# <a name="closesession"></a>CloseSession

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Termina una sesión con un clúster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Parámetros

_SessionId_
  
> El identificador de la sesión para cerrar. Este valor debe coincidir con el valor devuelto por [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si ha cerrado la sesión; **xlHpcRetInvalidSessionId** si el argumento de _SessionId_ no es válido; **xlHpcRetCallFailed** en otros errores. 
  
## <a name="see-also"></a>Vea también

- [OpenSession](opensession.md)
- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

