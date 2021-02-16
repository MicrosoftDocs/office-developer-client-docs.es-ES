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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407000"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una nueva [estructura MAPIUID](mapiuid.md) que se usará como identificador único. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parámetros

 _lpMuid_
  
> Puntero a la nueva **estructura MAPIUID.** 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se creó **la nueva estructura MAPIUID.** 
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::NewUID** se implementa para todos los objetos de compatibilidad. Los proveedores de servicios y los servicios de mensajes llaman a **NewUID** siempre que necesiten generar un identificador único a largo plazo. Un proveedor de almacén de mensajes, por ejemplo, puede llamar a **NewUID** para obtener **un MAPIUID** para colocar en la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de un mensaje recién creado.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No confunda la estructura **MAPIUID** que se registra durante el inicio de sesión con las estructuras **MAPIUID** que crea el **método NewUID.** La **estructura MAPIUID** que se registra al llamar al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) representa la libreta de direcciones o el proveedor del almacén de mensajes a MAPI y se usa para distinguir los identificadores de entrada que crean los distintos proveedores. Esta **estructura MAPIUID** debe codificarse de forma sólida y no obtenerse a través de una llamada a **NewUID**.
  
## <a name="see-also"></a>Consulte también



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

