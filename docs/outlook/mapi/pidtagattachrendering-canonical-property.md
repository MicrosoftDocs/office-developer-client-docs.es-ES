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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361099"
---
# <a name="pidtagattachrendering-canonical-property"></a>Propiedad canónica PidTagAttachRendering

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un metarchivo de Microsoft Windows con información de representación de datos adjuntos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Identificador:  <br/> |0x3709  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

La finalidad de esta propiedad es proporcionar un icono u otra representación gráfica que puede mostrarse dentro del mensaje primario en el punto de datos adjuntos. Esta representación suele incluir el nombre de los datos adjuntos, si los hay, y la naturaleza de los datos adjuntos, como un documento de Microsoft Office Word. Una aplicación cliente puede usar esta representación para mostrar el mensaje. 
  
Para un archivo adjunto, esta propiedad suele ilustrar un icono para el archivo. 
  
Para un mensaje adjunto, esta propiedad no suele establecerse. Una aplicación cliente que necesita representar un mensaje adjunto debe obtener su propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), llamar a [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para un puntero al objeto de información de formulario correspondiente, Abra la interfaz [IMAPIFormInfo](imapiforminfoimapiprop.md) en ese objeto y use **GetProps** para recuperar la propiedad **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) o **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
  
Para un objeto OLE estático incrustado, esta propiedad contiene un metarchivo de Microsoft Windows que se puede utilizar para dibujar la representación de datos adjuntos en una ventana. 
  
Para un objeto OLE dinámico incrustado, el cliente debe usar los datos OLE para generar la información de representación. 
  
En todos los casos, la aplicación cliente debe tener en cuenta que esta propiedad suele tener un tamaño de varios cientos de bytes y está sujeta a truncamiento en la tabla de datos adjuntos. Si un cliente desea representar los datos adjuntos desde esta propiedad sin abrir los datos adjuntos en sí, debe funcionar dentro de la regla de truncamiento de tablas. Para obtener más información, vea [trabajar con columnas de gran tamaño](working-with-large-columns.md). 
  
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

