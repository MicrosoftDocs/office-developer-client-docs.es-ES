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
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818009"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**Hace referencia a**: Outlook 
  
Indica si el proveedor de transporte ha recibido uno o más mensajes entrantes.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Parámetros

 _lpulIncoming_
  
> [out] Un valor que indica la existencia de mensajes de entrada. Un valor distinto de cero indica que no hay mensajes entrantes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama periódicamente al método de **IXPLogon::Poll** si el proveedor de transporte indica que se debe sondear para nuevos mensajes, que el proveedor pasando el LOGON_SP_POLL marcar a la llamada a la [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) método al principio de una sesión. Si el proveedor de transporte que se indica en respuesta a la llamada de **sondeo** que hay uno o más mensajes de entrada disponibles para él al proceso, la cola MAPI llama al método [IXPLogon::StartMessage](ixplogon-startmessage.md) para permitir que al proveedor de proceso de la primera entrada Mensaje. El proveedor de transporte indica mensajes entrantes estableciendo el valor en el parámetro _lpulIncoming_ en un valor distinto de cero. 
  
## <a name="see-also"></a>Vea también



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

