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
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419992"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza cambios permanentes en una sección de perfil del almacén de mensajes.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que indica el tipo de almacén de mensajes. Se puede establecer la siguiente marca:
    
MDB_TEMPORARY 
  
> El almacén de mensajes es temporal y no debe agregarse a la tabla de almacén de mensajes. Cuando se establece MDB_TEMPORARY, **ModifyProfile** Devuelve S_OK inmediatamente. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los cambios en la sección de perfil se han realizado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: ModifyProfile** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes llaman a **ModifyProfile** para solicitar a MAPI que modifique su información de perfil. 
  
 **ModifyProfile** agrega la sección de perfil asociada con el proveedor de llamadas a la lista de recursos de proveedor de almacén de mensajes instalados. Esto hace que el almacén de mensajes aparezca en la tabla de almacén de mensajes, que está disponible para los clientes a través del método [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) , y que se debe abrir sin mostrar un cuadro de diálogo. 
  
Si se establece la marca MDB_TEMPORARY, MAPI no realiza ninguna acción y el método vuelve inmediatamente con S_OK.
  
## <a name="see-also"></a>Ver también



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

