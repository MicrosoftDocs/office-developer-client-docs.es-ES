---
title: Propiedad canónica PidTagResourceFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330187"
---
# <a name="pidtagresourceflags-canonical-property"></a>Propiedad canónica PidTagResourceFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de máscara de marcas para servicios de mensajes y proveedores.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificador:  <br/> |0x3009  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Common MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad describe las características de un servicio de mensajes, un proveedor de servicios o un objeto de estado. Las marcas que se establecen para esta propiedad dependen de su contexto. Por ejemplo, algunas marcas solo son válidas para los objetos de estado y otros indicadores sólo para las columnas de la tabla de servicio de mensajes. 
  
Las marcas son de tres clases: Static, modificable y Dynamic. MAPI establece las marcas estáticas a partir de los datos de MAPISVC. INF y nunca se modificó. MAPI establece las marcas modificables desde MAPISVC. INF, pero puede cambiarse posteriormente. Los métodos MAPI pueden establecer y restablecer marcas dinámicas.
  
Para un servicio de mensajes, se pueden establecer uno o varios de los siguientes indicadores en esta propiedad:
  
SERVICE_CREATE_WITH_STORE 
  
> Reservado. No usar.
    
SERVICE_DEFAULT_STORE 
  
> Forma. El servicio de mensajes contiene el almacén predeterminado. Se debe mostrar una interfaz de usuario para pedir confirmación al usuario antes de eliminar o mover este servicio del perfil. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Static. El marcador de nivel de servicio que se debe establecer para indicar que ninguno de los proveedores del servicio de mensajes se puede usar para proporcionar una identidad. Se debe establecer esta marca o SERVICE_PRIMARY_IDENTITY, pero no ambas.
    
SERVICE_PRIMARY_IDENTITY 
  
> Modificable. El servicio de mensajes correspondiente contiene el proveedor usado para la identidad principal de esta sesión. Use [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para establecer esta marca. Se debe establecer esta marca o SERVICE_NO_PRIMARY_IDENTITY, pero no ambas. 
    
SERVICE_SINGLE_COPY 
  
> Static. Cualquier intento de crear o copiar este servicio de mensajes en un perfil en el que el servicio ya existe producirá un error. Para crear un servicio de mensaje de copia único, agregue la propiedad **PR_RESOURCE_FLAGS** a la sección del servicio en MAPISVC. INF y establece esta marca. 
    
Para un proveedor de servicios, se pueden establecer uno o varios de los siguientes indicadores en **PR_RESOURCE_FLAGS**:
  
HOOK_INBOUND 
  
> Static. El enlace de la cola de impresión debe procesar los mensajes entrantes.
    
HOOK_OUTBOUND 
  
> Static. El enlace de la cola de impresión debe procesar los mensajes salientes. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Modificable. Esta identidad debe aplicarse a los mensajes salientes si el perfil contiene varias instancias de este proveedor de transporte. Esto puede ocurrir si varias instancias de un único proveedor de transporte aparecen en el perfil.
    
STATUS_DEFAULT_STORE 
  
> Modificable. Este almacén de mensajes es el almacén predeterminado para el perfil. 
    
STATUS_NEED_IPM_TREE 
  
> Forma. Las carpetas estándar de este almacén de mensajes, incluida la carpeta raíz del mensaje interpersonal (IPM), todavía no se han comprobado. MAPI establece y borra esta marca. 
    
STATUS_NO_DEFAULT_STORE 
  
> Static. Este almacén de mensajes no puede convertirse en el almacén de mensajes predeterminado para el perfil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Static. Este proveedor no proporciona una identidad en su fila de estado. Se debe establecer esta marca o STATUS_PRIMARY_IDENTITY.
    
STATUS_OWN_STORE 
  
> Static. Este proveedor de transporte está estrechamente acoplado a un almacén de mensajes y proporciona la propiedad **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) en su fila de estado.
    
STATUS_PRIMARY_IDENTITY 
  
> Modificable. Este proveedor suministra la identidad principal para la sesión; el identificador de entrada para el objeto que suministra la identidad se devuelve desde [IMAPISession:: QueryIdentity](imapisession-queryidentity.md). Se debe establecer esta marca o **STATUS_NO_PRIMARY_IDENTITY** . 
    
STATUS_PRIMARY_STORE 
  
> Modificable. Este almacén de mensajes se debe usar cuando una aplicación cliente inicie sesión. Una vez abierto, este almacén debe establecerse como el almacén predeterminado para el perfil. 
    
STATUS_SECONDARY_STORE 
  
> Modificable. Este almacén de mensajes debe usarse si el almacén principal no está disponible cuando una aplicación cliente inicia sesión. Una vez abierto, este almacén debe establecerse como el almacén predeterminado para el perfil. 
    
STATUS_SIMPLE_STORE 
  
> Forma. Simple MAPI usará este almacén de mensajes como almacén de mensajes predeterminado.
    
STATUS_TEMP_SECTION 
  
> Forma. Este almacén de mensajes no debe publicarse en la tabla de almacén de mensajes y se eliminará del perfil tras el cierre de sesión. 
    
STATUS_XP_PREFER_LAST 
  
> Static. Este transporte espera ser el último transporte seleccionado para enviar un mensaje cuando varios proveedores de transporte puedan transmitir el mensaje.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propiedad canónica PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

