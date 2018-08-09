---
title: Propiedad canónica PidTagPstConfigurationFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b5a3978741f7ecb871e3c3de28e52dffdcf3a74f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819975"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Propiedad canónica PidTagPstConfigurationFlags
  
**Hace referencia a**: Outlook 
  
Especifica los indicadores de configuración para una tabla de almacenamiento de información personal (archivos .pst).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Identificador:  <br/> |0x6770  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabla de almacenamiento personal (.pst) interno  <br/> |
   
## <a name="remarks"></a>Comentarios

Las siguientes son valores válidos para esta propiedad:
  
PST_CONFIG_UNICODE
  
> Indica un archivo .pst Unicode. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Cuando set desde el cliente de marcas para el método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , **ConfigureMsgService** la trata como una llamada de [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) y omite la "este servicio de información no se ha configurado" advertencia. 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Indica a **ConfigureMsgService** para no cambiar el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), incluso aunque lo suministró. En ese caso, que ha proporcionado únicamente para los nuevos archivos pst.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Indica el código de configuración al primer para mostrar un cuadro de diálogo para confirmar si un archivo de carpetas sin conexión (.ost) se ha encontrado y, según la respuesta del usuario, o bien usar la carpeta que se encuentra sin conexión o habilitar al usuario para buscar otra carpeta sin conexión.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Copia el archivo .ost con un nuevo nombre único y descarta el nombre actual. El archivo .ost existente permanece en el equipo, pero ya no se usa en este perfil. Normalmente, esto se produce cuando Microsoft Outlook ya no se permite un archivo .ost determinado y las directivas del registro no permitir al usuario que cambie el nombre del archivo. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]] 
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

