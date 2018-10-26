---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3d45c4722b6a0200ea3937ba606da0af5c793df2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581856"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Recupera un valor que indica si el control de botón está habilitado o deshabilitado.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulState_
  
> [out] Un puntero a un valor que indica el estado del control de botón. Puede devolver uno de los siguientes valores:
    
MAPI_DISABLED 
  
> El control botón está deshabilitado y no se puede hacer clic en ella. 
    
MAPI_ENABLED 
  
> El control botón está habilitado y se puede hacer clic.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado del control de botón se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

Proveedores de servicios de implementan el método **IMAPIControl::GetState** para proporcionar MAPI con el estado de un control de botón. Si el botón está habilitado, puede responder a un clic del mouse o una pulsación de tecla. Si está deshabilitada, el botón aparece atenuado y no responde a un clic del mouse o una pulsación de tecla. 
  
Para obtener más información acerca de cómo implementar **GetState** y la otra [IMAPIControl: IUnknown](imapicontroliunknown.md) métodos, vea [Implementación de objeto de Control](control-object-implementation.md).
  
## <a name="see-also"></a>Vea también



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

