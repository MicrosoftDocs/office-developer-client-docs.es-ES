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
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411879"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una tabla de plantillas únicas para crear destinatarios que se agregarán a la lista de destinatarios de un mensaje saliente.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de columnas de cadena incluidas en la tabla. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no MAPI_UNICODE marca, las columnas de cadena tienen el formato ANSI.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de un solo acceso.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla única se recuperó correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y el proveedor de libreta de direcciones no admite Unicode o MAPI_UNICODE no se estableció y el proveedor de libreta de direcciones solo admite Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de libreta de direcciones no proporciona plantillas únicas.
    
## <a name="remarks"></a>Comentarios

MAPI llama al **método GetOneOffTable** para que las plantillas únicas estén disponibles para crear destinatarios. Los nuevos destinatarios se agregan a la lista de destinatarios de un mensaje saliente. Los proveedores de libreta de direcciones deben admitir la notificación en su tabla de uso único para informar a MAPI de las modificaciones de plantilla. MAPI mantiene abierta la tabla de uso único para habilitar la actualización dinámica. 
  
Los proveedores de libreta de direcciones también pueden admitir una tabla de uso único para cada uno de sus contenedores. Los autores de llamadas recuperan esta tabla única llamando al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor y solicitando la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Las plantillas disponibles a través de esta tabla se usan para agregar destinatarios al contenedor. Para obtener una explicación de las diferencias entre los dos tipos de tablas únicas, vea [Implementing One-Off Tables](implementing-one-off-tables.md).
  
Para obtener una lista de las columnas necesarias en la tabla única de un proveedor de libreta de direcciones, vea [One-Off Tables](one-off-tables.md).
  
## <a name="see-also"></a>Vea también



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

