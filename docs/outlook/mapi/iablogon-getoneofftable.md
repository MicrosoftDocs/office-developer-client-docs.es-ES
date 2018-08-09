---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b8a6d74df3749a5445d95ad392f7f88d27190bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817099"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Hace referencia a**: Outlook 
  
Devuelve un objeto table de plantillas de uso único para la creación de los destinatarios que se agregará a la lista de destinatarios de un mensaje saliente.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de columnas de cadena que se incluyen en la tabla. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las columnas de cadena se encuentran en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de uso único.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla de uso único se recuperó correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y el proveedor de la libreta de direcciones no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y el proveedor de la libreta de direcciones admite sólo Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de la libreta de direcciones no proporciona las plantillas de uso único.
    
## <a name="remarks"></a>Comentarios

MAPI llama al método de **GetOneOffTable** para hacer que las plantillas de uso único disponibles para crear a los destinatarios. Los destinatarios nuevos se agregan a la lista de destinatarios de un mensaje saliente. Los proveedores de la libreta de direcciones deben admitir la notificación en su tabla de uso único para informar a MAPI de las modificaciones de plantilla. MAPI mantiene en la tabla de uso único abierta para habilitar la actualización dinámica. 
  
Los proveedores de la libreta de direcciones también pueden admitir una tabla de uso único para cada uno de sus contenedores. Los autores de llamadas recuperar esta tabla de uso único, llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor y solicite la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Las plantillas disponibles en esta tabla se usan para agregar a destinatarios al contenedor. Para obtener una descripción de las diferencias entre los dos tipos de tablas de uso único, vea [Implementación de tablas de uso único](implementing-one-off-tables.md).
  
Para obtener una lista de las columnas necesarias en la tabla de uso único de un proveedor libreta de direcciones, vea [Las tablas de uso único](one-off-tables.md).
  
## <a name="see-also"></a>Vea también



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

