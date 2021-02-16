---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437542"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra una estructura [MAPIUID](mapiuid.md) que representa de forma única el proveedor de servicios. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpProviderID_
  
> [entrada] Puntero a la estructura **MAPIUID** que identifica la libreta de direcciones o el proveedor del almacén de mensajes. 
    
 _ulFlags_
  
> Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La **estructura MAPIUID** se registró correctamente. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::SetProviderUID** se implementa para objetos de compatibilidad con la libreta de direcciones y el proveedor del almacén de mensajes. Estos proveedores llaman **a SetProviderUID** para registrar un identificador único descrito en la estructura **MAPIUID** a la que apunta  _lpProviderID_. Los proveedores incluyen este identificador en todos los identificadores de entrada que crean. 
  
MAPI usa la **estructura MAPIUID** cuando envía mensajes salientes a la cola MAPI y para determinar el proveedor adecuado para controlar las solicitudes de cliente. Por ejemplo, cuando un cliente llama al método [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI examina la parte **MAPIUID** del identificador de entrada, la asigna al proveedor que lo pasó a **SetProviderUID** y llama a **OpenEntry** de ese proveedor. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame **a SetProviderUID** durante el inicio de sesión para registrar la **estructura MAPIUID.** MAPI permite a los proveedores de libretas de direcciones y al almacén de mensajes registrar varios identificadores. Cuando realiza varias llamadas a **SetProviderUID,** siempre agrega la estructura **MAPIUID** al conjunto del proveedor de estructuras **MAPIUID,** incluso si **MAPIUID** es un duplicado. **SetProviderUID** no puede quitar **un MAPIUID**. 
  
## <a name="see-also"></a>Consulte también



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

