---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b16730681b5414f28ae45be7195b4fa551bf0e82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591992"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hace que los cambios realizados en un mensaje de almacenar permanente de sección de perfil.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Almacenar una máscara de bits de marcadores que indica el tipo de mensaje. Se puede establecer la marca siguiente:
    
MDB_TEMPORARY 
  
> El almacén de mensajes es temporal y no debe agregarse a la tabla de almacenamiento de mensajes. Cuando se establece MDB_TEMPORARY, **ModifyProfile** devuelve S_OK inmediatamente. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los cambios realizados en la sección de perfil se realizaron correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::ModifyProfile** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes. Mensaje de llamada de los proveedores de almacén de **ModifyProfile** para solicitar MAPI para modificar la información de su perfil. 
  
 **ModifyProfile** agrega la sección de perfil que está asociada con el proveedor de llamada a la lista de recursos de proveedor de almacén de mensaje instalados. Esto hace que el almacén de mensajes que se mostrarán en la tabla de almacén de mensajes, que está disponible para los clientes a través del método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) y que se abra sin la presentación de un cuadro de diálogo. 
  
Si se establece la marca MDB_TEMPORARY, MAPI no realiza ninguna acción y el método devuelve inmediatamente con S_OK.
  
## <a name="see-also"></a>Recursos adicionales



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

