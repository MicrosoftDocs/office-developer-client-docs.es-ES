---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417864"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia el proceso de cierre de sesión. 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados. Si se devuelve algo que no S_OK, el proveedor ha cerrado sesión.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon::TransportLogoff** para finalizar una sesión de proveedor de transporte para un usuario determinado. Antes de llamar **a TransportLogoff,** la cola MAPI descarta los datos sobre los tipos de direcciones de mensajería compatibles para esta sesión pasada en el método [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El proveedor de transporte debe estar preparado para aceptar una llamada a **TransportLogoff** en cualquier momento. Si hay un mensaje en proceso, el proveedor debe detener el proceso de envío. 
  
El proveedor de transporte debe liberar todos los recursos asignados para su sesión actual. Si ha asignado alguna memoria para esta sesión con la función [MAPIAllocateBuffer,](mapiallocatebuffer.md) debe liberar la memoria mediante la [función MAPIFreeBuffer.](mapifreebuffer.md) Cualquier memoria asignada por el proveedor de transporte para satisfacer las llamadas al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) se puede liberar de forma segura en este momento. 
  
Normalmente, al completar una llamada **TransportLogoff,** un proveedor primero debe invalidar su objeto de inicio de sesión llamando al método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) y, a continuación, liberar su objeto de soporte técnico. La implementación del proveedor de **TransportLogoff** debe liberar el objeto de soporte técnico en último lugar, ya que cuando se libera el objeto de compatibilidad, la cola MAPI también puede liberar el propio objeto de proveedor. 
  
## <a name="see-also"></a>Vea también



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

