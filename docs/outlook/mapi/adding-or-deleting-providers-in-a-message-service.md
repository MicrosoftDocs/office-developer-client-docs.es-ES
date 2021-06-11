---
title: Agregar o eliminar proveedores en un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433426"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Agregar o eliminar proveedores en un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para agregar o eliminar proveedores de servicios en un servicio de mensajes, use la [interfaz IProviderAdmin : IUnknown.](iprovideradminiunknown.md) Puede recuperar un puntero **IProviderAdmin** llamando a [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). La tabla del proveedor, a la que se puede obtener acceso a través [de IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md)muestra información sobre los proveedores de servicios instalados actualmente en el servicio de mensajes. Los clientes y proveedores de servicios pueden usar la tabla de proveedores para obtener acceso al nombre del archivo DLL del proveedor, por ejemplo, o **mapiuid**, nombre para mostrar y tipo del proveedor, así como información sobre el servicio de mensajes. Para obtener más información, vea [Tablas de proveedor](provider-tables.md).
  
 **Para agregar o eliminar un proveedor de servicios en un servicio de mensajes**
  
1. Llame al **método AdminServices** para obtener acceso a un objeto de administración del servicio de mensajes. 
    
2. Llame [a IMsgServiceAdmin::GetMsgServiceTable para](imsgserviceadmin-getmsgservicetable.md) obtener acceso a la tabla de servicio de mensajes. 
    
3. Cree una restricción de propiedad mediante una estructura [SPropertyRestriction](spropertyrestriction.md) que coincida con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) con el nombre del servicio de mensajes que se va a modificar. 
    
4. Llame al método [IMAPITable::FindRow](imapitable-findrow.md) de la tabla de servicio de mensajes para buscar la fila de la tabla que representa el servicio de mensajes de destino. 
    
5. Llama [a IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) para recuperar un **puntero IProviderAdmin.** Pase la **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila de tabla de servicio de mensajes como parámetro _lpUID._ 
    
6. Llame [a IProviderAdmin::GetProviderTable para](iprovideradmin-getprovidertable.md) obtener acceso a la tabla del proveedor. 
    
7. Cree una restricción de propiedad mediante una estructura SPropertyRestriction que coincida con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) con el nombre del proveedor de servicios que se va a agregar o eliminar. 
    
8. Llame al método [IMAPITable::FindRow](imapitable-findrow.md) de la tabla de proveedor para buscar la fila de la tabla que representa el proveedor de servicios de destino. 
    
9. Llame [a IProviderAdmin::CreateProvider para](iprovideradmin-createprovider.md) agregar el proveedor o [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md) para quitarlo del servicio de mensajes. Para **CreateProvider,** pase la propiedad **PR_DISPLAY_NAME** del proveedor como el parámetro _lpszProvider._ Para cualquiera de los dos métodos, pase la propiedad **PR_SERVICE_UID** del proveedor como parámetro _lpUID._ Después de agregar o eliminar el proveedor de servicios, el cambio no será aparente hasta que se cree una nueva sesión. 
    
Otra técnica para agregar un proveedor de servicios, específicamente un proveedor de almacén de mensajes, a un perfil implica la construcción de un identificador de entrada para el proveedor. Dado que la construcción de un identificador de entrada requiere conocimiento de su formato, esta técnica solo se puede usar si el proveedor de servicios ha hecho público su formato de identificador de entrada. 
  
Con el identificador de entrada recién construido, un cliente puede llamar a [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI crea automáticamente una sección de perfil en el perfil para el proveedor de servicios, pero no la agrega a un servicio de mensajes. 
  
Algunos servicios de mensajes no permiten este tipo de modificación dinámica; si se admite o no está en el servicio de mensajes. Otra característica que puede o no ser compatible es la capacidad de acceder directamente a las secciones de perfil privado de un servicio de mensajes. Si el servicio de mensajes que está usando permite dicho acceso, publicará el **GUID** que representa la sección privada en MAPISVC.INF. Puede pasar este **GUID en** una llamada a [IProviderAdmin::OpenProfileSection para](iprovideradmin-openprofilesection.md) obtener acceso a la sección de perfil. 
  

