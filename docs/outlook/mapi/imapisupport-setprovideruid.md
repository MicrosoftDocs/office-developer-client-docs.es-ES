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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326316"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra una estructura [MAPIUID](mapiuid.md) que representa exclusivamente al proveedor de servicios. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpProviderID_
  
> a Puntero a la estructura **MAPIUID** que identifica la libreta de direcciones o el proveedor de almacenamiento de mensajes. 
    
 _ulFlags_
  
> Reserve debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La estructura **MAPIUID** se registró correctamente. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: SetProviderUID** se implementa para los objetos de compatibilidad de la libreta de direcciones y del proveedor de almacenamiento de mensajes. Estos proveedores llaman a **SetProviderUID** para registrar un identificador único que se describe en la estructura **MAPIUID** a la que apunta _lpProviderID_. Los proveedores incluyen este identificador en todos los identificadores de entrada que crean. 
  
MAPI usa la estructura **MAPIUID** cuando envía mensajes salientes a la cola MAPI y determina el proveedor adecuado para controlar las solicitudes de los clientes. Por ejemplo, cuando un cliente llama al método [IMAPISession:: OpenEntry](imapisession-openentry.md) , MAPI examina la parte **MAPIUID** del identificador de la entrada, la asigna al proveedor que la pasó a **SetProviderUID**y llama a la **OpenEntry** del proveedor. . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame a **SetProviderUID** en el momento del inicio de sesión para registrar la estructura de **MAPIUID** . MAPI permite que la libreta de direcciones y los proveedores de almacenamiento de mensajes registren varios identificadores. Cuando se realizan varias llamadas a **SetProviderUID**, siempre se agrega la estructura **MAPIUID** al conjunto de estructuras **MAPIUID** del proveedor, incluso si el **MAPIUID** es un duplicado. **SetProviderUID** no puede quitar un **MAPIUID**. 
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

