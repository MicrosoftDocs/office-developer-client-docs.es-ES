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
ms.openlocfilehash: 14be41c21244abe8c54261a95a410828c973d66b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817517"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

