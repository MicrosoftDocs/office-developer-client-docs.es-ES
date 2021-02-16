---
title: Identidad principal mapi
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5bf88de280b012c54d4caaac6bdfe877f476ac37
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404725"
---
# <a name="mapi-primary-identity"></a>Identidad principal mapi

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La mayoría de las sesiones MAPI tienen un proveedor de servicios determinado que proporciona la identidad principal de la sesión. Normalmente, es un proveedor de libretas de direcciones, que proporciona identidad a través de uno de sus objetos de usuario de mensajería o listas de distribución. De hecho, MAPI recomienda que los servicios de mensajes que incluyen un proveedor de libreta de direcciones usen uno de sus objetos para la identidad principal. Cuando un proveedor de servicios que pertenece a un servicio de mensajes proporciona la identidad principal, todos los demás proveedores de servicios del servicio de mensajes comparten esta identidad.
  
The MAPISVC. El archivo de configuración inf tiene entradas relacionadas con la identidad en el nivel del servicio de mensajes y del proveedor de servicios. Las secciones del servicio de mensajes deben incluir una entrada que indica si el servicio puede suministrar la identidad principal; las secciones del proveedor de servicios incluyen una entrada similar solo cuando el proveedor puede proporcionar una identidad.
  
En la tabla siguiente se enumeran las entradas que aparecen en las secciones servicio de mensajes y proveedor de servicios en MAPISVC. Archivo INF.
  
|**Proveedor de identidad principal**|**PR_RESOURCE_FLAGS configuración**|
|:-----|:-----|
|Servicio de mensajes  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|No es el servicio de mensajes  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Proveedor de servicios  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Aunque varios servicios de mensajes pueden declarar su capacidad para proporcionar la identidad principal de una sesión, solo se selecciona un servicio de mensajes para hacerlo. Esta selección puede producirse:
  
- Cuando se crea un perfil.
    
- Cuando un cliente llama a **IMsgServiceAdmin::SetPrimaryIdentity** para establecer explícitamente un servicio de mensajes determinado como proveedor de la identidad de la sesión. Para obtener más información. Vea [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Cuando se crea un perfil, MAPI designa el primer servicio de mensajes que se configurará que incluye un proveedor con la marca STATUS_PRIMARY_IDENTITY establecida en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) para proporcionar la identidad principal. Dentro del servicio de mensajes designado, se elige el primer proveedor que se configurará con este conjunto de marcas de recursos para proporcionar la identidad del servicio. La STATUS_PRIMARY_IDENTITY se borra para todos los demás proveedores del servicio designado y otros servicios de mensajes en el perfil. Si en cualquier momento se quita del perfil el proveedor que suministra la identidad principal, MAPI asigna el rol al siguiente proveedor para configurarlo que puede suministrar la identidad. Esto viene determinado por la apariencia de la entrada en la sección del proveedor  `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` en MAPISVC.INF. 
  
Cuando un cliente llama al método **IMsgServiceAdmin::SetPrimaryIdentity** de un servicio de mensajes, especifica el MAPIUID de un proveedor de servicios dentro del servicio de destino. Para obtener más información, vea [MAPIUID](mapiuid.md). El proveedor de servicios representado por **MAPIUID** se asigna para proporcionar la identidad principal para el servicio de mensajes y para la sesión, y todos los demás proveedores del servicio compartirán esta identidad. 
  
Cada proveedor del servicio de mensajes responsable de suministrar la identidad principal actualiza su fila en la tabla de estado para incluir las siguientes propiedades.
  
|**Propiedad de identidad principal**|**Establecer como**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nombre para mostrar del objeto que proporciona la identidad principal.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Clave de búsqueda para el objeto que proporciona la identidad principal.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificador de entrada del objeto que proporciona la identidad principal.  <br/> |
   
 **Para recuperar el identificador de entrada del objeto que proporciona la identidad principal**
  
- Llame al **método IMAPISession::QueryIdentity.** Para obtener más información, [vea IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** busca en la tabla de estado la fila que contiene el valor STATUS_PRIMARY_IDENTITY  en su columna **PR_RESOURCE_FLAGS** y devuelve el PR_IDENTITY_ENTRYID correspondiente como identificador de entrada de la identidad principal. 
    

