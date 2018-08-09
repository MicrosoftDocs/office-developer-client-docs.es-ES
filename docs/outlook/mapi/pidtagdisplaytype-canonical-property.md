---
title: Propiedad canónica PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3fd5a8d92621dcefce66fb42e843f78755fa84df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819461"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Propiedad canónica PidTagDisplayType

  
  
**Hace referencia a**: Outlook 
  
Contiene un valor que se utiliza para asociar un icono a una fila de una tabla determinada. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Identificador:  <br/> |0x3900  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene un número entero largo que facilita un tratamiento especial de la entrada de la tabla en función de su tipo. Este tratamiento especial suele consta de mostrar un icono u otro elemento de presentación, asociado con el tipo de visualización. 
  
Esta propiedad no se usa en las tablas de contenido de carpeta. Aplicaciones cliente deben usar la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) y la interfaz [IMAPIFormInfo](imapiforminfoimapiprop.md) adecuada de un mensaje para obtener la **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) y **PR_MINI_ICON** ([ PidTagMiniIcon](pidtagminiicon-canonical-property.md)) las propiedades de ese mensaje. 
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
DT_AGENT 
  
> Un agente automatizado, como oferta del día o una presentación de gráfico del tiempo.
    
DT_DISTLIST 
  
> Una lista de distribución.
    
DT_FOLDER 
  
> Muestra el icono de carpeta predeterminada adyacente a la carpeta.
    
DT_FOLDER_LINK 
  
> Mostrar el icono de vínculo de carpeta predeterminado adyacente a la carpeta en lugar del icono de carpeta predeterminado.
    
DT_FOLDER_SPECIAL 
  
> Muestra el icono de una carpeta con una distinción específicos de la aplicación, como un tipo especial de carpeta pública.
    
DT_FORUM 
  
> Un foro, como un servicio de boletín electrónico o una carpeta pública o compartida.
    
DT_GLOBAL 
  
> Una libreta de direcciones global.
    
DT_LOCAL 
  
> Una libreta de direcciones local que se comparte con un pequeño grupo de trabajo.
    
DT_MAILUSER 
  
> Un usuario típico de mensajería.
    
DT_MODIFIABLE 
  
> Modificable; el contenedor debe indicado como modificable en la interfaz de usuario.
    
DT_NOT_SPECIFIC 
  
> No coincide con ninguno de los otros valores.
    
DT_ORGANIZATION 
  
> Un alias especial definido para un grupo de gran tamaño, como coordinador de la unidad de sangre, Contabilidad o departamento de soporte técnico.
    
DT_PRIVATE_DISTLIST 
  
> Privado, personalmente administran la lista de distribución.
    
DT_REMOTE_MAILUSER 
  
> Destinatario que se conocen como desde un sistema de mensajería externo o remoto.
    
DT_WAN 
  
> Una libreta de direcciones de red de área extensa.
    
Tablas de contenido de la libreta de direcciones utilizan los valores DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST y DT_REMOTE_MAILUSER. Tablas de jerarquía de la libreta de direcciones y tablas de uso único usan los valores DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC y DT_WAN. Tablas de jerarquía de carpeta use los valores DT_FOLDER, DT_FOLDER_LINK y DT_FOLDER_SPECIAL. 
  
Si no se establece esta propiedad, el cliente debe asumir el tipo predeterminado apropiado para la tabla, normalmente DT_FOLDER, DT_LOCAL o DT_MAILUSER. 
  
 **Nota** Todos los valores no documentados están reservados para MAPI. Las aplicaciones cliente no deben definir los nuevos valores y deben estar preparadas abordar los problemas con un valor sin documentar. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para las plantillas de la libreta de direcciones.
    
[[MS-OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Habilita el acceso de Active directory.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

