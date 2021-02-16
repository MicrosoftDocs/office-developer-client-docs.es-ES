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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436233"
---
# <a name="pidtagresourceflags-canonical-property"></a>Propiedad canónica PidTagResourceFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas para proveedores y servicios de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificador:  <br/> |0x3009  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mapi común  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad describe las características de un servicio de mensajes, un proveedor de servicios o un objeto de estado. Las marcas que se establecen para esta propiedad dependen de su contexto. Por ejemplo, algunas marcas solo son válidas para los objetos de estado y otras solo para las columnas de la tabla de servicio de mensajes. 
  
Las marcas son de tres clases: estática, modificable y dinámica. MAPI establece las marcas estáticas a partir de los datos de MAPISVC. INF y nunca modificado. MAPI establece las marcas modificables desde MAPISVC. INF, pero se puede cambiar posteriormente. Los métodos MAPI pueden establecer y restablecer las marcas dinámicas.
  
Para un servicio de mensajes, se pueden establecer una o varias de las siguientes marcas en esta propiedad:
  
SERVICE_CREATE_WITH_STORE 
  
> Reservado. No usar.
    
SERVICE_DEFAULT_STORE 
  
> Dinámico. El servicio de mensajes contiene el almacén predeterminado. Debe mostrarse una interfaz de usuario solicitando confirmación al usuario antes de eliminar o mover este servicio fuera del perfil. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Estático. La marca de nivel de servicio que se debe establecer para indicar que ninguno de los proveedores del servicio de mensajes se puede usar para proporcionar una identidad. Esta marca o SERVICE_PRIMARY_IDENTITY deben establecerse, pero no ambas.
    
SERVICE_PRIMARY_IDENTITY 
  
> Modificable. El servicio de mensajes correspondiente contiene el proveedor usado para la identidad principal de esta sesión. Use [IMsgServiceAdmin::SetPrimaryIdentity para](imsgserviceadmin-setprimaryidentity.md) establecer esta marca. Esta marca o SERVICE_NO_PRIMARY_IDENTITY deben establecerse, pero no ambas. 
    
SERVICE_SINGLE_COPY 
  
> Estático. Se producirá un error en cualquier intento de crear o copiar este servicio de mensajes en un perfil en el que ya exista el servicio. Para crear un servicio de mensaje de copia **única, agregue PR_RESOURCE_FLAGS** propiedad a la sección del servicio en MAPISVC. INF y establece esta marca. 
    
Para un proveedor de servicios, se pueden establecer una o varias de las siguientes marcas en **PR_RESOURCE_FLAGS:**
  
HOOK_INBOUND 
  
> Estático. El enlace de cola debe procesar los mensajes entrantes.
    
HOOK_OUTBOUND 
  
> Estático. El enlace de cola debe procesar los mensajes salientes. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Modificable. Esta identidad debe aplicarse a los mensajes salientes si el perfil contiene varias instancias de este proveedor de transporte. Esto puede suceder si aparecen varias instancias de un único proveedor de transporte en el perfil.
    
STATUS_DEFAULT_STORE 
  
> Modificable. Este almacén de mensajes es el almacén predeterminado para el perfil. 
    
STATUS_NEED_IPM_TREE 
  
> Dinámico. Las carpetas estándar de este almacén de mensajes, incluida la carpeta raíz del mensaje interpersonal (IPM), aún no se han comprobado. MAPI establece y borra esta marca. 
    
STATUS_NO_DEFAULT_STORE 
  
> Estático. Este almacén de mensajes no es capaz de convertirse en el almacén de mensajes predeterminado para el perfil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Estático. Este proveedor no proporciona una identidad en su fila de estado. Esta marca o STATUS_PRIMARY_IDENTITY deben establecerse.
    
STATUS_OWN_STORE 
  
> Estático. Este proveedor de transporte está estrechamente unido a un almacén de mensajes y proporciona la propiedad **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) en su fila de estado.
    
STATUS_PRIMARY_IDENTITY 
  
> Modificable. Este proveedor ofrece la identidad principal de la sesión; el identificador de entrada del objeto que ofrece la identidad se devuelve de [IMAPISession::QueryIdentity](imapisession-queryidentity.md). Esta marca o **STATUS_NO_PRIMARY_IDENTITY** deben establecerse. 
    
STATUS_PRIMARY_STORE 
  
> Modificable. Este almacén de mensajes se debe usar cuando una aplicación cliente inicia sesión. Una vez abierto, este almacén debe establecerse como el almacén predeterminado para el perfil. 
    
STATUS_SECONDARY_STORE 
  
> Modificable. Este almacén de mensajes se usará si el almacén principal no está disponible cuando una aplicación cliente inicia sesión. Una vez abierto, este almacén debe establecerse como el almacén predeterminado para el perfil. 
    
STATUS_SIMPLE_STORE 
  
> Dinámico. Simple MAPI usará este almacén de mensajes como almacén de mensajes predeterminado.
    
STATUS_TEMP_SECTION 
  
> Dinámico. Este almacén de mensajes no debe publicarse en la tabla del almacén de mensajes y se eliminará del perfil después de cerrar sesión. 
    
STATUS_XP_PREFER_LAST 
  
> Estático. Este transporte espera ser el último transporte seleccionado para enviar un mensaje cuando varios proveedores de transporte puedan transmitir el mensaje.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propiedad canónica PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

