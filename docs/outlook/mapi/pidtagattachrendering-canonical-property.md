---
title: Propiedad canónica PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383194"
---
# <a name="pidtagattachrendering-canonical-property"></a>Propiedad canónica PidTagAttachRendering

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene un metarchivo de Microsoft Windows con la información de representación de los datos adjuntos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Identificador:  <br/> |0x3709  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

El propósito de esta propiedad es proporcionar un icono u otra representación gráfica que se puede mostrar dentro del mensaje primario en el punto de datos adjuntos. La representación normalmente incluye el nombre de los datos adjuntos, si lo hay y la naturaleza de los datos adjuntos, como un documento de Microsoft Office Word. Una aplicación cliente puede utilizar esta representación en la visualización del mensaje. 
  
Para un archivo adjunto, esta propiedad normalmente representa un icono para el archivo. 
  
Para un mensaje adjunto, esta propiedad no se establece normalmente. Una aplicación de cliente que se necesitan representar un mensaje adjunto debe obtener su propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), llame a [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para un puntero al objeto de información de formulario correspondiente, Abra la interfaz de [IMAPIFormInfo](imapiforminfoimapiprop.md) en ese objeto y use **GetProps** para recuperar la propiedad de **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)). 
  
Para un objeto OLE incrustado estático, esta propiedad contiene un metarchivo de Microsoft Windows que se puede usar para dibujar la representación de datos adjuntos en una ventana. 
  
Para un objeto OLE incrustado dinámico, el cliente debe utilizar los datos OLE para generar la información de representación. 
  
En todos los casos, la aplicación cliente deben tener en cuenta que esta propiedad suele ser varios cientos de bytes en tamaño y está sujeta a truncamiento en la tabla de datos adjuntos. Si un cliente desea representar los datos adjuntos de esta propiedad sin abrir los datos adjuntos del propio, debe trabajar dentro de la regla de truncamiento de tabla. Para obtener más información, vea [trabajar con columnas de gran tamaño](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
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

