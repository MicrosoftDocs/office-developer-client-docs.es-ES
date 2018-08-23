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
ms.openlocfilehash: 244087c41e33e470c42434e9d57cee7317bcb78c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571692"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una nueva estructura [MAPIUID](mapiuid.md) que se utilizará como un identificador único. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parámetros

 _lpMuid_
  
> Un puntero a la nueva estructura **MAPIUID** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado la nueva estructura **MAPIUID** . 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::NewUID** se implementa para todos los objetos de soporte técnico. Proveedores de servicio y servicios de mensajes de llamada **NewUID** cada vez que se necesitan para generar un identificador único a largo plazo. Un mensaje de almacenar proveedor, por ejemplo, puede llamar a **NewUID** para obtener un **MAPIUID** para poner en la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de un mensaje recién creado.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Es importante no confundir la estructura **MAPIUID** que registrar en tiempo de inicio de sesión con las estructuras **MAPIUID** que crea el método **NewUID** . La estructura **MAPIUID** que registrar cuando se llama al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) representa la libreta de direcciones o mensaje de proveedor MAPI de almacén y se usa para distinguir los identificadores de entrada que crean proveedores diferentes. Esta estructura **MAPIUID** debe ser codificado de forma rígida y no se obtienen a través de una llamada a **NewUID**.
  
## <a name="see-also"></a>Recursos adicionales



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

