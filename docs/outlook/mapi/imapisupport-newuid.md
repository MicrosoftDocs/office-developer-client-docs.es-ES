---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330201"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una nueva estructura [MAPIUID](mapiuid.md) para usarla como identificador único. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parameters

 _lpMuid_
  
> Un puntero a la nueva estructura **MAPIUID** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado la nueva estructura **MAPIUID** . 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: NewUID** se implementa para todos los objetos de compatibilidad. Los proveedores de servicios y los servicios de mensajes llaman a **NewUID** cada vez que necesitan generar un identificador único a largo plazo. Un proveedor de almacenamiento de mensajes, por ejemplo, puede llamar a **NewUID** para obtener una **MAPIUID** para colocarla en la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de un mensaje recién creado.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No confunda la estructura **MAPIUID** que se registra en el momento de inicio de sesión con las estructuras **MAPIUID** que crea el método **NewUID** . La estructura **MAPIUID** que se registra cuando se llama al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) representa su libreta de direcciones o proveedor de almacenamiento de mensajes en MAPI y se usa para distinguir los identificadores de entrada que crean proveedores distintos. Esta estructura **MAPIUID** debe estar codificada de forma rígida y no obtenerse a través de una llamada a **NewUID**.
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

