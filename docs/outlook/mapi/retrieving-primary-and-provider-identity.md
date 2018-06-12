---
title: Recuperar la identidad de proveedor y primaria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 2a87e32fe21aa6fb1d9296c568a74da994c146bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820520"
---
# <a name="retrieving-primary-and-provider-identity"></a>Recuperar la identidad de proveedor y primaria

  
  
**Se aplica a**: Outlook 
  
Proveedores de servicios, normalmente proveedores de libreta de direcciones, tienen la opción de proporcionar una identidad que puede usarse para representar la sesión en una gran variedad de situaciones. Tres propiedades describen la identidad de un proveedor:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Estas propiedades se establecen en el identificador de entrada, el nombre para mostrar y la clave de búsqueda del objeto identity correspondiente, que normalmente es un usuario de mensajería. Proveedores que suministran una identidad también establecer la marca STATUS_PRIMARY_IDENTITY en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
Dependiendo de sus necesidades, podría usar la identidad de un determinado proveedor o la identidad principal para la sesión. Puede usar la identidad de un proveedor también para fines de presentación o para recuperar las propiedades, como **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, si establece, contiene la ruta de acceso a archivos usa o creada por el proveedor. Recupere la propiedad **PR_RESOURCE_PATH** para el proveedor de proporcionar la identidad principal cuando desea ubicar los archivos que pertenecen al usuario de la sesión. 
  
 **Para recuperar la identidad de un proveedor específico**
  
1. Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Crear una restricción de uso de una estructura de [SPropertyRestriction](spropertyrestriction.md) para que coincida con la columna **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) con el nombre del proveedor especificado. 
    
3. Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para localizar fila del proveedor en la. Identidad del proveedor se almacenará en la columna **PR_IDENTITY_ENTRYID** , si existe. 
    
 **Para recuperar la identidad principal para una sesión**
  
- Llame a [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** bases de identidad de la sesión de la existencia del valor STATUS_PRIMARY_IDENTITY en la columna **PR_RESOURCE_FLAGS** de una de las filas de la tabla de estado. Si ninguna de las filas de estado tienen definido este valor, **QueryIdentity** asigna la identidad para el primer proveedor de servicios que establece las tres propiedades PR_IDENTITY. Si ningún proveedor de servicio proporciona una identidad, **QueryIdentity** devuelve MAPI_W_NO_SERVICE. Cuando esto sucede, debe crear una cadena de caracteres para representar un usuario genérico que puede servir como la identidad principal. 
    
 **Para establecer explícitamente la identidad principal para una sesión**
  
- Llame a [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Pase el **MAPIUID** para el proveedor de servicio de destino. 
    

