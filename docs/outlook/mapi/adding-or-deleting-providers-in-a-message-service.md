---
title: Agregar o eliminar los proveedores de servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 05d6d548032476062127f21b23aa2ce141ed1b65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816397"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Agregar o eliminar los proveedores de servicio de mensajes

  
  
**Hace referencia a**: Outlook 
  
Para agregar o eliminar proveedores de servicios en un servicio de mensajes, use el [IProviderAdmin: IUnknown](iprovideradminiunknown.md) interfaz. Puede recuperar un puntero **IProviderAdmin** mediante una llamada a [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). En la tabla de proveedor, puede tener acceso a través de [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), se muestra información acerca de los proveedores de servicios instalados actualmente en el servicio de mensajes. Los clientes y proveedores de servicios pueden usar la tabla de proveedor para tener acceso al nombre de proveedor archivo DLL, por ejemplo, o el **MAPIUID**, el nombre para mostrar y el tipo de proveedor así como información sobre el servicio de mensajes. Para obtener más información, vea [Las tablas de proveedor](provider-tables.md).
  
 **Para agregar o eliminar un proveedor de servicios en un servicio de mensajes**
  
1. Llame al método **AdminServices** para obtener acceso a un objeto de administración del servicio de mensajes. 
    
2. Llame a [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener acceso a la tabla de mensajes de servicio. 
    
3. Crear una restricción de propiedad utilizando una estructura [SPropertyRestriction](spropertyrestriction.md) que coincide con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) con el nombre del servicio de mensaje que se va puede modificar. 
    
4. Llamar al método [IMAPITable:: FindRow](imapitable-findrow.md) de la tabla de servicio de mensaje para buscar la fila en la tabla que representa el servicio de mensajes de destino. 
    
5. Llame a [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) para recuperar un puntero **IProviderAdmin** . Pasar la columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila de tabla del servicio de mensajes como el parámetro _lpUID_ . 
    
6. Llame a [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) para obtener acceso a la tabla de proveedores. 
    
7. Crear una restricción de propiedad utilizando una estructura SPropertyRestriction que coincide con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) con el nombre del proveedor de servicios para que sea Agregar o eliminar. 
    
8. Llamar al método [IMAPITable:: FindRow](imapitable-findrow.md) de la tabla proveedor para buscar la fila en la tabla que representa el proveedor de servicio de destino. 
    
9. Llamar a [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) para agregar el proveedor o [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md) para quitar desde el servicio de mensajes. Para **CreateProvider**, pase la propiedad del proveedor **PR_DISPLAY_NAME** como el parámetro _lpszProvider_ . Para cualquiera de los métodos, pase la propiedad del proveedor **PR_SERVICE_UID** como el parámetro _lpUID_ . Después de que se ha agregado o eliminado el proveedor de servicios, el cambio no será evidente hasta que se crea una nueva sesión. 
    
Otra técnica para agregar un proveedor de servicios, específicamente un proveedor de almacén de mensajes, a un perfil implica la construcción de un identificador de entrada para el proveedor. Debido a que la construcción de un identificador de entrada requiere conocimientos de su formato, esta técnica sólo puede utilizarse si el proveedor de servicios realizados por su formato de identificador de entrada pública. 
  
Con el identificador de entrada recién construido, un cliente puede llamar a [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI automáticamente crea una sección de perfil en el perfil para el proveedor de servicios, pero no lo agrega a un servicio de mensaje. 
  
Algunos servicios de mensajes no permitir a este tipo de modificación dinámica; Si no es compatible con es hasta el servicio de mensajes. Otra característica que puede o no es posible que se admite es la capacidad de tener acceso directamente a las secciones de perfil privado de un servicio de mensaje. Si está utilizando el servicio de mensajes permite este tipo de acceso, publicará el **GUID** que representa la sección privada en MAPISVC.INF. Puede pasar este **GUID** en una llamada a [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) para tener acceso a la sección de perfil. 
  

