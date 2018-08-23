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
ms.openlocfilehash: cb9a2ba72ee9fd9c45aefe9d0797930a4871404a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579287"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se abre el objeto de estado del proveedor.
  
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
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se debe utilizar para tener acceso al objeto de estado. Pasando NULL devuelve la interfaz del objeto estándar, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto de estado. Se puede establecer la marca siguiente:
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren con acceso de solo lectura y los autores de llamadas no deben asumir que se ha concedido permiso de lectura y escritura.
    
 _lpulObjType_
  
> [out] Un puntero al tipo del objeto abierto.
    
 _lppEntry_
  
> [out] Un puntero a un puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y se ha abierto el objeto de estado.
    
## <a name="remarks"></a>Comentarios

Los proveedores de la libreta de direcciones implementan el método **OpenStatusEntry** para conceder acceso a su objeto de estado. Todos los proveedores de libreta de direcciones son necesarios para implementar un objeto de estado que admite, como mínimo, el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . Para obtener más información, vea [Implementación de objeto de estado](status-object-implementation.md).
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

