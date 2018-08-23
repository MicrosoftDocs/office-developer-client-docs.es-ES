---
title: Identidad principal de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de1fe8fd5ef5a6e79934478c62b2403c48f85b5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565882"
---
# <a name="mapi-primary-identity"></a>Identidad principal de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La mayoría de las sesiones MAPI tienen un proveedor de servicio en particular que proporciona la identidad principal para la sesión. Normalmente, es un proveedor de libreta de direcciones, que proporciona la identidad a través de uno de sus objetos de usuario de mensajería o listas de distribución. De hecho, MAPI se recomienda que los servicios de mensajes que incluyen un proveedor de la libreta de direcciones usar uno de sus objetos para la identidad principal. Cuando un proveedor de servicios que pertenece a un servicio de mensaje proporciona la identidad principal, todos los otros proveedores de servicio en el servicio de mensajes de compartan esta identidad.
  
El archivo MAPISVC. Archivo de configuración de INF tiene entradas relacionado con la identidad en el servicio de mensajes y el nivel de proveedor de servicio. Las secciones de servicio del mensaje deben incluir una entrada que indica si el servicio puede proporcionar la identidad principal; las secciones de proveedor de servicio incluyen una entrada similar sólo cuando el proveedor puede proporcionar una identidad.
  
En la siguiente tabla se enumera las entradas que aparecen en el servicio de mensajes y las secciones de proveedor de servicio en el archivo MAPISVC. Archivo INF.
  
|**Proveedor de identidad principal**|**Configuración de PR_RESOURCE_FLAGS**|
|:-----|:-----|
|Servicio de mensajes  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|No es el servicio de mensajes  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Proveedor de servicios  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Aunque varios servicios de mensaje pueden declarar su capacidad de proporcionar identidad principal de la sesión, el servicio de un solo mensaje se selecciona para hacerlo. Puede producirse esta selección:
  
- Cuando se crea un perfil.
    
- Cuando un cliente llama a **IMsgServiceAdmin::SetPrimaryIdentity** para establecer explícitamente un servicio de mensaje determinado como el proveedor de la identidad de la sesión. Para obtener más información. Vea [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Cuando se crea un perfil, MAPI designa el primer servicio de mensajes para configurarse que incluye un proveedor con el indicador STATUS_PRIMARY_IDENTITY establecido en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) para proporcionar la identidad principal . Dentro del servicio de mensajes designados, se elige el primer proveedor de configurarse con este conjunto de marca de recursos para proporcionar la identidad para el servicio. El indicador STATUS_PRIMARY_IDENTITY está desactivado para todos los demás proveedores en el servicio designado y otros servicios de mensaje en el perfil. Si en cualquier momento se quita el proveedor de identidad principal de proporcionar el perfil, MAPI asigna el rol al siguiente proveedor configurarse que puede suministrar la identidad. Esto viene determinado por la apariencia de la `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` entrada en la sección del proveedor en MAPISVC.INF. 
  
Cuando un cliente llama a un mensaje **IMsgServiceAdmin::SetPrimaryIdentity** al método servicio, especifica el MAPIUID para un proveedor de servicio dentro del servicio de destino. Para obtener más información, vea [MAPIUID](mapiuid.md). El proveedor de servicios representado por el **MAPIUID** se asigna a proporcionar la identidad principal para el servicio de mensajes y de la sesión, y todos los otros proveedores en el servicio compartirá esta identidad. 
  
Cada proveedor en el servicio de mensajes responsable de suministrar la identidad principal actualiza su fila en la tabla de estado para incluir las siguientes propiedades.
  
|**Propiedad identidad principal**|**Establecer como**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nombre para mostrar del objeto proporcionar la identidad principal.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Clave de búsqueda para el objeto de proporcionar la identidad principal.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificador de entrada para el objeto de proporcionar la identidad principal.  <br/> |
   
 **Para recuperar el identificador de entrada para el objeto de proporcionar la identidad principal**
  
- Llame al método **IMAPISession::QueryIdentity** . Para obtener más información, vea [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** busca en la tabla de estado de la fila que contiene el valor STATUS_PRIMARY_IDENTITY en su columna **PR_RESOURCE_FLAGS** y devuelve el correspondiente **PR_IDENTITY_ENTRYID** como el identificador de entrada de la principal identidad. 
    

