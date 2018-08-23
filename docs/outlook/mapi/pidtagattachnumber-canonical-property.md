---
title: Propiedad canónica PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f6de157864bff5be41b6e030d555be7b60dcda5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594757"
---
# <a name="pidtagattachnumber-canonical-property"></a>Propiedad canónica PidTagAttachNumber

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un número que identifica de forma exclusiva los datos adjuntos en su mensaje primario. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_NUM  <br/> |
|Identificador:  <br/> |0x0E21  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Almacenes de mensaje generan y mantienen esta propiedad. El número de datos adjuntos es el criterio de ordenación secundario, después de la posición de representación, en la tabla de datos adjuntos. 
  
 **PR_ATTACH_NUM** se usa para abrir los datos adjuntos con el método [IMessage::OpenAttach](imessage-openattach.md) . Dentro de la sesión de la aplicación de cliente, la propiedad **PR_ATTACH_NUM** de datos adjuntos del mensaje permanece constante mientras está abierta en la tabla de datos adjuntos. 
  
El almacén de mensajes propaga los cambios a la tabla con los métodos **IMessage::CreateAttach** y **IMessage::DeleteAttach** . En su opción del almacén de mensajes puede generar notificaciones de tabla en las tablas de datos adjuntos abiertos para que los clientes pueden volver a sincronizar a esos cambios. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

