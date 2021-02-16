---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410787"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre el objeto de estado del proveedor.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Parámetros

 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se debe usar para tener acceso al objeto de estado. Pasar NULL devuelve la interfaz estándar del objeto, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se abre el objeto de estado. Se puede establecer la siguiente marca:
    
MAPI_MODIFY 
  
> Solicita permiso de lectura y escritura. De forma predeterminada, los objetos se abren con acceso de solo lectura y los autores de llamadas no deben suponer que se ha concedido permiso de lectura y escritura.
    
 _lpulObjType_
  
> [salida] Puntero al tipo del objeto abierto.
    
 _lppEntry_
  
> [salida] Puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y se ha abierto el objeto de estado.
    
## <a name="remarks"></a>Comentarios

Los proveedores de libretas de direcciones implementan **el método OpenStatusEntry** para conceder acceso a su objeto de estado. Todos los proveedores de libretas de direcciones son necesarios para implementar un objeto de estado que admita, como mínimo, el [método IMAPIStatus::ValidateState.](imapistatus-validatestate.md) Para obtener más información, vea [Implementación de objeto de estado.](status-object-implementation.md)
  
## <a name="see-also"></a>Consulte también



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

