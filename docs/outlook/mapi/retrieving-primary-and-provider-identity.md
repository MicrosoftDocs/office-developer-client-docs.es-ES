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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328640"
---
# <a name="retrieving-primary-and-provider-identity"></a>Recuperación de la identidad principal y del proveedor

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de servicios, por lo general, los proveedores de libreta de direcciones, tienen la opción de proporcionar una identidad que se puede usar para representar la sesión en diversas situaciones. Hay tres propiedades que describen la identidad de un proveedor:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Estas propiedades se establecen en el identificador de entrada, el nombre para mostrar y la clave de búsqueda del objeto de identidad correspondiente, que suele ser un usuario de mensajería. Los proveedores que proporcionan una identidad también establecen la marca STATUS_PRIMARY_IDENTITY en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
Según sus necesidades, puede usar una identidad de proveedor determinada o la identidad principal para la sesión. La identidad de un proveedor también se puede usar para fines de presentación o para recuperar propiedades, como **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, si se establece, contiene la ruta de acceso a los archivos usados o creados por el proveedor. Recupere la propiedad **PR_RESOURCE_PATH** para el proveedor que proporciona la identidad principal cuando desea localizar los archivos que pertenecen al usuario de la sesión. 
  
 **Para recuperar la identidad de un proveedor específico**
  
1. Llame a [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Cree una restricción con una estructura [SPropertyRestriction](spropertyrestriction.md) para que la columna **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) se corresponda con el nombre del proveedor especificado. 
    
3. Llame al método [IMAPITable:: FindRow](imapitable-findrow.md) para localizar la fila del proveedor. La identidad del proveedor se almacenará en la columna **PR_IDENTITY_ENTRYID** , si existe. 
    
 **Para recuperar la identidad principal de una sesión**
  
- Llamar a [IMAPISession:: QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** basa la identidad de sesión en la existencia del valor STATUS_PRIMARY_IDENTITY en la columna **PR_RESOURCE_FLAGS** de una de las filas de la tabla de estado. Si ninguna de las filas de Estado tiene este valor establecido, **QueryIdentity** asigna la identidad al primer proveedor de servicios que establece las tres propiedades PR_IDENTITY. Si ningún proveedor de servicios proporciona una identidad, **QueryIdentity** devuelve MAPI_W_NO_SERVICE. Cuando esto ocurre, debe crear una cadena de caracteres para representar un usuario genérico que puede actuar como la identidad principal. 
    
 **Para establecer explícitamente la identidad principal de una sesión**
  
- Llamar a [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Pase el **MAPIUID** para el proveedor de servicios de destino. 
    

