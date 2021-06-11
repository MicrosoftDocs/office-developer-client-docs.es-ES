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
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360784"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Propiedad canónica PidTagDisplayType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor usado para asociar un icono a una fila determinada de una tabla. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Identificador:  <br/> |0x3900  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene un entero largo que facilita el tratamiento especial de la entrada de tabla en función de su tipo. Este tratamiento especial suele consistir en mostrar un icono u otro elemento de visualización asociado con el tipo de presentación. 
  
Esta propiedad no se usa en las tablas de contenido de carpetas. Las aplicaciones cliente deben usar la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de un mensaje y la interfaz [IMAPIFormInfo](imapiforminfoimapiprop.md) adecuada para obtener las propiedades **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) y **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) para ese mensaje. 
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
DT_AGENT 
  
> Un agente automatizado, como La cita del día o una presentación de gráficos meteorológicos.
    
DT_DISTLIST 
  
> Una lista de distribución.
    
DT_FOLDER 
  
> Mostrar el icono de carpeta predeterminado adyacente a la carpeta.
    
DT_FOLDER_LINK 
  
> Mostrar el icono de vínculo de carpeta predeterminado adyacente a la carpeta en lugar del icono de carpeta predeterminado.
    
DT_FOLDER_SPECIAL 
  
> Icono de visualización de una carpeta con una distinción específica de la aplicación, como un tipo especial de carpeta pública.
    
DT_FORUM 
  
> Un foro, como un servicio de tablón de anuncios o una carpeta pública o compartida.
    
DT_GLOBAL 
  
> Una libreta de direcciones global.
    
DT_LOCAL 
  
> Una libreta de direcciones local que comparte con un grupo de trabajo pequeño.
    
DT_MAILUSER 
  
> Un usuario de mensajería típico.
    
DT_MODIFIABLE 
  
> Modificable; el contenedor debe anotarse como modificable en la interfaz de usuario.
    
DT_NOT_SPECIFIC 
  
> No coincide con ninguna de las otras opciones de configuración.
    
DT_ORGANIZATION 
  
> Alias especial definido para un grupo grande, como el departamento de soporte técnico, la contabilidad o el coordinador de sangre.
    
DT_PRIVATE_DISTLIST 
  
> Una lista de distribución privada y administrada personalmente.
    
DT_REMOTE_MAILUSER 
  
> Un destinatario conocido por ser de un sistema de mensajería externo o remoto.
    
DT_WAN 
  
> Una libreta de direcciones de red de área extensa.
    
Las tablas de contenido de la libreta de direcciones usan los DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST y DT_REMOTE_MAILUSER. Las tablas de jerarquía de libreta de direcciones y las tablas DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC y DT_WAN valores. Las tablas de jerarquía de carpetas usan DT_FOLDER, DT_FOLDER_LINK y DT_FOLDER_SPECIAL valores. 
  
Si no se establece esta propiedad, el cliente debe asumir el tipo predeterminado adecuado para la tabla, normalmente DT_FOLDER, DT_LOCAL o DT_MAILUSER. 
  
 **Nota** Todos los valores no documentados están reservados para MAPI. Las aplicaciones cliente no deben definir nuevos valores y deben estar preparadas para tratar con un valor no documentado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para las plantillas de libreta de direcciones.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Habilita el acceso a directorios.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

