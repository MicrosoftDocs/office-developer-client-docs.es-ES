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
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419012"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera un valor que indica si el control de botón está habilitado o deshabilitado.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulState_
  
> [salida] Puntero a un valor que indica el estado del control de botón. Se puede devolver uno de los siguientes valores:
    
MAPI_DISABLED 
  
> El control de botón está deshabilitado y no se puede hacer clic en el botón. 
    
MAPI_ENABLED 
  
> El control de botón está habilitado y se puede hacer clic en el botón.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado del control de botón se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

Los proveedores de servicios implementan **el método IMAPIControl::GetState** para proporcionar MAPI con el estado de un control de botón. Si el botón está habilitado, puede responder a un clic del mouse o presionar una tecla. Si está deshabilitado, el botón aparece atenuado y no responde a un clic del mouse ni a presionar una tecla. 
  
Para obtener más información acerca de cómo implementar **GetState** y los otros [métodos IMAPIControl : IUnknown,](imapicontroliunknown.md) vea [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Consulte también



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

