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
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327254"
---
# <a name="pidtagattachnumber-canonical-property"></a>Propiedad canónica PidTagAttachNumber

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un número que identifica de forma única los datos adjuntos dentro de su mensaje primario. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_NUM  <br/> |
|Identificador:  <br/> |0x0E21  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Los almacenes de mensajes generan y mantienen esta propiedad. El número de datos adjuntos es la clave de ordenación secundaria, después de la posición de representación, en la tabla de datos adjuntos. 
  
 **PR_ATTACH_NUM** se usa para abrir los datos adjuntos con el método [IMessage:: OpenAttach](imessage-openattach.md) . Dentro de la sesión de una aplicación cliente, la propiedad **PR_ATTACH_NUM** de un adjunto del mensaje permanece constante siempre que la tabla de datos adjuntos esté abierta. 
  
El almacén de mensajes propaga los cambios en la tabla mediante los métodos **IMessage:: CreateAttach** y **IMessage::D eleteattach** . En su opción, el almacén de mensajes puede generar notificaciones de tabla en tablas de datos adjuntos abiertas para que los clientes puedan volver a sincronizarse para esos cambios. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

