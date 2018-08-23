---
title: Propiedad canónica PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 629746cedf8c6f4a8c960912a9ab1bcdc7a09e9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574149"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Propiedad canónica PidTagAttachDataBinary

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene los datos adjuntos binarios normalmente tiene acceso a través de la interfaz de vinculación e incrustación de objetos (OLE) **IStream** . 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es ATTACH_BY_VALUE, que es el método habitual de datos adjuntos y el único que deben admitir. **PR_ATTACH_DATA_BIN** también contiene datos adjuntos OLE 1.0 **OLESTREAM** cuando el valor de **PR_ATTACH_METHOD** es ATTACH_OLE. 
  
 Datos adjuntos de **OLESTREAM** pueden copiarse en un archivo llamando al método OLE **IStream:: CopyTo** . El tipo de codificación de OLE puede estar determinado por la propiedad **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para datos adjuntos un archivo de documento OLE, el proveedor de almacenamiento de mensajes, debe responder a una llamada de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) y, opcionalmente, puede responder a una llamada en **PR_ATTACH_DATA_BIN **. Tenga en cuenta que **PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** compartan el mismo identificador de propiedad y, por tanto, son dos copias de la misma propiedad. 
  
Para un objeto de almacenamiento, como un archivo compuesto en el formato de archivo doc de OLE 2.0, algunos proveedores de servicios de permitir que se va a abrir con la interfaz de MAPI **IStreamDocfile** para mejorar el rendimiento. Un proveedor que admita **IStreamDocfile** debe exponerlo en **PR_ATTACH_DATA_OBJ** y, opcionalmente, puede exponer en **PR_ATTACH_DATA_BIN**. 
  
Para obtener más información sobre las interfaces OLE y formatos, vea [OLE y la transferencia de datos](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
## <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

