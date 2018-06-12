---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815519"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Informa el conector de clúster que se ha cancelado un cálculo de Excel y, por lo tanto, todos los pendientes llamadas a la función dentro de esa sesión es posible que se puede cancelar así como (y que Excel no espera las devoluciones de llamada con sus resultados).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Sintaxis

_SessionID_
  
> El identificador de la sesión usado por el cálculo cancelado. Este valor coincide con el valor devuelto por [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si el argumento de _SessionId_ es válido; **xlHpcRetInvalidSessionId** si el argumento de _SessionId_ no es válido; **xlHpcRetCallFailed** en otros errores. 
  
## <a name="remarks"></a>Notas

Los implementadores deben detener todos los procesos de la sesión para mejorar el rendimiento, como los resultados recibidos después de esta llamada se descartarán por Excel.
  
## <a name="see-also"></a>Ver también

- [Funciones de conector de clúster de Excel](excel-cluster-connector-functions.md)

