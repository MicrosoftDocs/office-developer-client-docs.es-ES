---
title: Adición o eliminación de proveedores en un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329564"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Adición o eliminación de proveedores en un servicio de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para agregar o eliminar proveedores de servicios en un servicio de mensajes, use la interfaz [IProviderAdmin: IUnknown](iprovideradminiunknown.md) . Puede recuperar un puntero **IProviderAdmin** llamando a [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md). La tabla de proveedores, a la que se puede obtener acceso a través de [IProviderAdmin:: GetProviderTable](iprovideradmin-getprovidertable.md), incluye información sobre los proveedores de servicios instalados actualmente en el servicio de mensajes. Los clientes y los proveedores de servicios pueden usar la tabla de proveedores para obtener acceso al nombre del archivo DLL del proveedor, por ejemplo, el **MAPIUID**, el nombre para mostrar y el tipo de proveedor, así como la información sobre el servicio de mensajes. Para obtener más información, vea [tablas de proveedor](provider-tables.md).
  
 **Para agregar o eliminar un proveedor de servicios en un servicio de mensajes**
  
1. Llame al método **AdminServices** para tener acceso a un objeto de administración del servicio de mensajes. 
    
2. Llame a [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener acceso a la tabla de servicio de mensajes. 
    
3. Cree una restricción de propiedad con una estructura [SPropertyRestriction](spropertyrestriction.md) que coincida con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) con el nombre del servicio de mensajes que se va a cambiado. 
    
4. Llame al método [IMAPITable:: FindRow](imapitable-findrow.md) de la tabla del servicio de mensajes para localizar la fila en la tabla que representa el servicio de mensajes de destino. 
    
5. Llamar a [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) para recuperar un puntero **IProviderAdmin** . Pase la columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila de la tabla de servicios de mensajes como el parámetro _lpUID_ . 
    
6. Llame a [IProviderAdmin:: GetProviderTable](iprovideradmin-getprovidertable.md) para obtener acceso a la tabla del proveedor. 
    
7. Cree una restricción de propiedad con una estructura SPropertyRestriction que coincida con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) con el nombre del proveedor de servicios que se va a Agregar o eliminar. 
    
8. Llame al método [IMAPITable:: FindRow](imapitable-findrow.md) de la tabla del proveedor para localizar la fila en la tabla que representa al proveedor de servicios de destino. 
    
9. Llame a [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md) para agregar el proveedor o [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md) para quitarlo del servicio de mensajes. Para **CreateProvider**, pase la propiedad **PR_DISPLAY_NAME** del proveedor como el parámetro _lpszProvider_ . Para cualquiera de estos métodos, pase la propiedad **PR_SERVICE_UID** del proveedor como el parámetro _lpUID_ . Una vez que se ha agregado o eliminado el proveedor de servicios, el cambio no se apreciará hasta que se cree una nueva sesión. 
    
Otra técnica para agregar un proveedor de servicios, en concreto un proveedor de almacenamiento de mensajes, a un perfil implica crear un identificador de entrada para el proveedor. Dado que la creación de un identificador de entrada requiere conocimientos de su formato, esta técnica solo se puede usar si el proveedor de servicios ha hecho público su formato de identificador de entrada. 
  
Con el identificador de entrada recién construido, un cliente puede llamar a [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md). MAPI crea automáticamente una sección de perfil en el perfil del proveedor de servicios, pero no la agrega a un servicio de mensajes. 
  
Algunos servicios de mensajes no permiten este tipo de modificación dinámica; Si se admite o no es el servicio de mensajes. Otra característica que puede o no puede admitirse es la capacidad de tener acceso directamente a las secciones de perfil privado del servicio de mensajes. Si el servicio de mensajes que está usando permite este tipo de acceso, publicará el **GUID** que representa la sección privada en el archivo MAPISVC. inf. Puede pasar este **GUID** en una llamada a [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) para obtener acceso a la sección de perfil. 
  

