---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414721"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Informa al conector de clúster de que se ha cancelado un cálculo de Excel y, por lo tanto, todas las llamadas de función pendientes dentro de esa sesión también se pueden cancelar (y que Excel no espera devoluciones de llamada con sus resultados).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Parameters

_SessionID_
  
> Identificador de la sesión usada por el cálculo cancelado. Este valor coincide con el valor devuelto por [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si el  _argumento SessionId_ es válido; **xlHpcRetInvalidSessionId** si el  _argumento SessionId_ no es válido; **xlHpcRetCallFailed en** otros errores. 
  
## <a name="remarks"></a>Comentarios

Los implementadores deben detener todos los procesos de la sesión para mejorar el rendimiento, ya que los resultados recibidos después de esta llamada se descartarán Excel.
  
## <a name="see-also"></a>Vea también

- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

