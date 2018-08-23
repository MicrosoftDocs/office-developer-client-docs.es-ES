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
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578019"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica que el sistema está inactivo, habilitar el proveedor de transporte realizar operaciones de prioridad baja.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama periódicamente el método **IXPLogon::Idle** , si solicitado durante las horas de cuando el sistema está inactivo, se pasa el indicador XP_LOGON_SP en la llamada al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) que abrió la sesión actual. A veces cuando el sistema está inactivo, el proveedor de transporte puede realizar operaciones en segundo plano que no son adecuados durante el resto de las llamadas a o de que se producen de forma regular. 
  
## <a name="see-also"></a>Recursos adicionales



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

