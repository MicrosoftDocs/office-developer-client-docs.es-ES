---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425277"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si el proveedor de transporte ha recibido uno o más mensajes de entrada.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Parameters

 _lpulIncoming_
  
> contempla Un valor que indica la existencia de mensajes entrantes. Un valor distinto de cero indica que hay mensajes entrantes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama periódicamente al método **IXPLogon::P Oll** si el proveedor de transporte indica que debe realizarse un sondeo de los nuevos mensajes, que el proveedor realiza pasando la marca LOGON_SP_POLL a la llamada a [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) al principio de una sesión. Si el proveedor de transporte indica en respuesta a **** la llamada de sondeo que hay uno o más mensajes entrantes disponibles para que los procese, la cola MAPI llama al método [IXPLogon:: StartMessage](ixplogon-startmessage.md) para permitir que el proveedor procese el primer entrada mensaje. El proveedor de transporte indica los mensajes entrantes estableciendo el valor del parámetro _lpulIncoming_ en un valor distinto de cero. 
  
## <a name="see-also"></a>Ver también



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

