---
title: Recuperación de la identidad principal y del proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430815"
---
# <a name="retrieving-primary-and-provider-identity"></a>Recuperación de la identidad principal y del proveedor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de servicios, normalmente proveedores de libretas de direcciones, tienen la opción de proporcionar una identidad que se puede usar para representar la sesión en una variedad de situaciones. Tres propiedades describen la identidad de un proveedor:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Estas propiedades se establecen en el identificador de entrada, el nombre para mostrar y la clave de búsqueda del objeto de identidad correspondiente, que suele ser un usuario de mensajería. Los proveedores que suministran una identidad también establecen la marca STATUS_PRIMARY_IDENTITY en su **propiedad PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
Según sus necesidades, puede usar la identidad de un proveedor en particular o la identidad principal para la sesión. También puede usar la identidad de un proveedor para mostrar o recuperar propiedades, como **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, si se establece, contiene la ruta de acceso a los archivos usados o creados por el proveedor. Recupere la **PR_RESOURCE_PATH** para el proveedor que proporciona la identidad principal cuando desee buscar archivos que pertenezcan al usuario de la sesión. 
  
 **Para recuperar la identidad de un proveedor específico**
  
1. Llame [a IMAPISession::GetStatusTable para](imapisession-getstatustable.md) obtener acceso a la tabla de estado. 
    
2. Cree una restricción mediante una estructura [SPropertyRestriction](spropertyrestriction.md) para que coincida con la columna **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) con el nombre del proveedor especificado. 
    
3. Llame [a IMAPITable::FindRow](imapitable-findrow.md) para buscar la fila del proveedor. La identidad del proveedor se almacenará en la **PR_IDENTITY_ENTRYID,** si existe. 
    
 **Para recuperar la identidad principal de una sesión**
  
- Llame [a IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** basa la identidad de sesión en la existencia del valor STATUS_PRIMARY_IDENTITY en la columna **PR_RESOURCE_FLAGS** para una de las filas de la tabla de estado. Si ninguna de las filas de estado tiene este valor establecido, **QueryIdentity** asigna identidad al primer proveedor de servicios que establece las tres PR_IDENTITY propiedades. Si ningún proveedor de servicios proporciona una identidad, **QueryIdentity** devuelve MAPI_W_NO_SERVICE. Cuando esto sucede, debe crear una cadena de caracteres para representar un usuario genérico que pueda servir como identidad principal. 
    
 **Para establecer explícitamente la identidad principal de una sesión**
  
- Llame [a IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Pase **mapiuid** para el proveedor de servicios de destino. 
    

