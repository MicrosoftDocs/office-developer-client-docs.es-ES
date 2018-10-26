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
ms.openlocfilehash: 761228a01e0dc778b962c62436e872ff20d72088
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586315"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Inicia el proceso de cierre de sesión. 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores. Si no se devuelve nada distinto de S_OK, el proveedor se cerró.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPLogon::TransportLogoff** para finalizar una sesión de proveedor de transporte de un usuario concreto. Antes de llamar a **TransportLogoff**, la cola MAPI descarta los datos acerca de los tipos de dirección de mensajería admitidos para esta sesión pasada en el método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El proveedor de transporte debe estar preparado para aceptar una llamada a **TransportLogoff** en cualquier momento. Si un mensaje está en proceso, el proveedor debe detener el proceso de envío. 
  
El proveedor de transporte debe liberar todos los recursos asignados para la sesión actual. Si ha asignado la memoria para esta sesión con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que debe liberar la memoria mediante el uso de la función [MAPIFreeBuffer](mapifreebuffer.md) . Puede liberar memoria asignada por el proveedor de transporte para satisfacer las llamadas al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) sin ningún riesgo en este momento. 
  
Normalmente, en completar una llamada **TransportLogoff** , un proveedor debe invalidar primero su objeto de inicio de sesión llamando al método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) y, a continuación, de su objeto de compatibilidad con la versión. La implementación del proveedor de **TransportLogoff** debe liberar el objeto de soporte técnico por última vez, ya que cuando se libera el objeto de soporte, la cola MAPI también puede liberar el objeto de proveedor de sí mismo. 
  
## <a name="see-also"></a>Vea también



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

