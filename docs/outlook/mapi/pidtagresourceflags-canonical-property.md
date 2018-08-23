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
ms.openlocfilehash: 875b37183134a6c5beca76ab7910cf601d1b6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567506"
---
# <a name="pidtagresourceflags-canonical-property"></a>Propiedad canónica PidTagResourceFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de indicadores para servicios de mensajes y proveedores.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificador:  <br/> |0x3009  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comunes  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad describe las características de un servicio de mensajes, un proveedor de servicios o un objeto de estado. Los indicadores que se han establecido para esta propiedad dependen de su contexto. Por ejemplo, algunas marcas son válidos únicamente para los objetos de estado y otros marcadores sólo para las columnas en la tabla de servicios de mensaje. 
  
Los marcadores son de tres clases: estáticos, modificable y dinámicos. Se establecen indicadores estáticas por MAPI desde los datos en MAPISVC. INF y nunca se modifica. Se establecen indicadores modificables por MAPI desde MAPISVC. INF pero se puede cambiar posteriormente. Marcas dinámicos se pueden establecer y restablecer por métodos MAPI.
  
Para un servicio de mensajes, se pueden establecer en esta propiedad uno o varios de los siguientes indicadores:
  
SERVICE_CREATE_WITH_STORE 
  
> Reservado. No la use.
    
SERVICE_DEFAULT_STORE 
  
> Dinámico. El servicio de mensajes contiene el almacén predeterminado. Una interfaz de usuario debe mostrarse preguntar al usuario la confirmación antes de eliminar o mover este servicio fuera de los perfiles. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Static. El indicador de nivel de servicio que se debe establecer para indicar que ninguno de los proveedores en el servicio de mensajes se puede usar para proporcionar una identidad. Este indicador o el SERVICE_PRIMARY_IDENTITY debe ser set, pero no ambos.
    
SERVICE_PRIMARY_IDENTITY 
  
> Puede modificar. El servicio de mensajes correspondiente contiene el proveedor que se utiliza para la identidad principal de esta sesión. Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para establecer esta marca. Este indicador o el SERVICE_NO_PRIMARY_IDENTITY debe ser set, pero no ambos. 
    
SERVICE_SINGLE_COPY 
  
> Static. Se producirá un error en cualquier intento para crear o copiar este servicio de mensajes a un perfil de ubicación donde ya existe el servicio. Para crear una copia de un solo servicio de mensajes agregar la propiedad **PR_RESOURCE_FLAGS** a la sección del servicio MAPISVC. INF y establezca esta marca. 
    
Para un proveedor de servicios, se pueden establecer en **PR_RESOURCE_FLAGS**uno o varios de los siguientes indicadores:
  
HOOK_INBOUND 
  
> Static. El enlace de la cola de impresión debe procesar los mensajes entrantes.
    
HOOK_OUTBOUND 
  
> Static. El enlace de la cola de impresión necesita para procesar los mensajes salientes. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Puede modificar. Esta identidad debe aplicarse a los mensajes salientes si el perfil contiene varias instancias de este proveedor de transporte. Esto puede ocurrir si varias instancias de un proveedor de transporte único aparecen en el perfil.
    
STATUS_DEFAULT_STORE 
  
> Puede modificar. Este almacén de mensajes es el almacén predeterminado para el perfil. 
    
STATUS_NEED_IPM_TREE 
  
> Dinámico. Aún no se ha comprobado las carpetas estándar en este almacén de mensajes, incluyendo la carpeta raíz de mensajes interpersonales (IPM). MAPI establece y borra este indicador. 
    
STATUS_NO_DEFAULT_STORE 
  
> Static. Este almacén de mensajes es capaz de convertirse en el almacén de mensajes predeterminado para el perfil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Static. Este proveedor no proporcionar una identidad en su fila de estado. Se debe establecer este indicador o STATUS_PRIMARY_IDENTITY.
    
STATUS_OWN_STORE 
  
> Static. Este proveedor de transporte se complementa con un almacén de mensajes y proporciona la propiedad **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) en la fila de estado correspondiente.
    
STATUS_PRIMARY_IDENTITY 
  
> Puede modificar. Este proveedor aporta la identidad principal para la sesión; se devuelve el identificador de entrada para el objeto de suministro de la identidad de [IMAPISession::QueryIdentity](imapisession-queryidentity.md). Se debe establecer este indicador o **STATUS_NO_PRIMARY_IDENTITY** . 
    
STATUS_PRIMARY_STORE 
  
> Puede modificar. Este almacén de mensajes es para usarse cuando una aplicación cliente inicia sesión. Una vez abierto, se debe establecer este almacén como el almacén predeterminado para el perfil. 
    
STATUS_SECONDARY_STORE 
  
> Puede modificar. Este almacén de mensajes es que se usará si el almacén principal no está disponible cuando una aplicación cliente inicia sesión. Una vez abierto, se debe establecer este almacén como el almacén predeterminado para el perfil. 
    
STATUS_SIMPLE_STORE 
  
> Dinámico. Como su almacén de mensajes de forma predeterminada, se usará este almacén de mensajes mediante Simple MAPI.
    
STATUS_TEMP_SECTION 
  
> Dinámico. Este almacén de mensajes no se debe publicar en la tabla de almacén de mensajes y se eliminarán del perfil de después de cierre de sesión. 
    
STATUS_XP_PREFER_LAST 
  
> Static. Este transporte espera que sea la última transporte seleccionado para enviar un mensaje cuando varios proveedores de transporte se pueden transmitir el mensaje.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propiedad canónica PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

