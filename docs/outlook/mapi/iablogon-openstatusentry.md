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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349024"
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

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se debe usar para obtener acceso al objeto status. Al pasar NULL, se devuelve la interfaz estándar del objeto, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre el objeto status. Se puede establecer la siguiente marca:
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, los objetos se abren con acceso de solo lectura y las personas que llaman no suponen que se ha concedido el permiso de lectura y escritura.
    
 _lpulObjType_
  
> contempla Un puntero al tipo del objeto abierto.
    
 _lppEntry_
  
> contempla Un puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y se ha abierto el objeto de estado.
    
## <a name="remarks"></a>Comentarios

Los proveedores de la libreta de direcciones implementan el método **OpenStatusEntry** para conceder acceso a su objeto status. Se necesitan todos los proveedores de la libreta de direcciones para implementar un objeto de estado que admita, como mínimo, el método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) . Para obtener más información, vea [implementación de objetos de estado](status-object-implementation.md).
  
## <a name="see-also"></a>Vea también



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

