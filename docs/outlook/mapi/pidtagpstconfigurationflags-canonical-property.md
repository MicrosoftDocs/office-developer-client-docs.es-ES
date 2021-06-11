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
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408946"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Propiedad canónica PidTagPstConfigurationFlags
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica las marcas de configuración de una tabla de almacenamiento personal (archivo .pst).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Identificador:  <br/> |0x6770  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabla de almacenamiento personal (.pst) interna  <br/> |
   
## <a name="remarks"></a>Comentarios

Los siguientes son valores válidos para esta propiedad:
  
PST_CONFIG_UNICODE
  
> Indica un archivo .pst Unicode. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Cuando se establece de las marcas de cliente al método [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md) **trata ConfigureMsgService** como una llamada [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) y omite la advertencia "Este servicio de información no se ha configurado". 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Indica **a ConfigureMsgService** que no cambie el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), aunque se haya proporcionado. En ese caso, solo se suministró para los nuevos archivos .pst.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Indica al código de configuración que primero muestre un cuadro de diálogo para confirmar si se encontró un archivo de carpeta sin conexión (.ost) y, según la respuesta del usuario, use la carpeta sin conexión encontrada o habilite al usuario para buscar otra carpeta sin conexión.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Copia el archivo .ost con un nuevo nombre único y descarta el nombre actual. El archivo .ost existente permanece en el equipo, pero ya no se usa en este perfil. Esto suele ocurrir cuando Microsoft Outlook permite un archivo .ost determinado y las directivas del Registro no permiten al usuario cambiar el nombre del archivo. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]] 
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

