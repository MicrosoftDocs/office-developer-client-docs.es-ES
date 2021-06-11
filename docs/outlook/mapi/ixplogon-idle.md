---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436051"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica que el sistema está inactivo, lo que permite al proveedor de transporte realizar operaciones de baja prioridad.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama periódicamente al método **IXPLogon::Idle,** si se solicita, durante las horas en las que el sistema está inactivo pasando la marca XP_LOGON_SP en la llamada al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) que abrió la sesión actual. En ocasiones, cuando el sistema está inactivo, el proveedor de transporte puede realizar operaciones en segundo plano que no son apropiadas durante otras llamadas o que deben producirse de forma regular. 
  
## <a name="see-also"></a>Vea también



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

