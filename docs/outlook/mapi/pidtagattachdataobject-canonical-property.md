---
title: Propiedad canónica PidTagAttachDataObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3fc7690a8c9eb2ada3a34bc44217ff463721e4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819212"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Propiedad canónica PidTagAttachDataObject

  
  
**Hace referencia a**: Outlook 
  
Contiene un objeto attachment normalmente tiene acceso a través de la interfaz de vinculación e incrustación de objetos (OLE) **IStorage** . 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es **ATTACH_EMBEDDED_MSG** o **ATTACH_OLE**. Desde **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)), se puede determinar el tipo de codificación de OLE. 
  
Para los datos adjuntos asociados con el valor **ATTACH_EMBEDDED_MSG** , se puede usar la interfaz [IMessage:IMAPIProp](imessageimapiprop.md) para un acceso más rápido. 
  
Para un objeto OLE incrustado dinámico, la propiedad **PR_ATTACH_DATA_OBJ** contiene su propia información de representación y debe ser la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) que no existe o está vacía. 
  
Para los datos adjuntos un archivo de documento OLE, el proveedor de almacén de mensajes, debe responder a una llamada de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en **PR_ATTACH_DATA_OBJ** y, opcionalmente, puede responder a una llamada en **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ). Las propiedades **PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** compartan el mismo identificador de propiedad y, por tanto, son dos copias de la misma propiedad. 
  
Para un objeto de almacenamiento, como un archivo compuesto en el formato de archivo doc de OLE 2.0, algunos proveedores de servicios de permitir que se va a abrir con la interfaz de MAPI **IStreamDocfile** , una subclase de **IStream** sin miembros adicionales, diseñado para optimizar el rendimiento. El ahorro potencial es suficiente para justificar al intentar abrir **PR_ATTACH_DATA_OBJ** a través de **IStreamDocfile**. Si se devuelve **MAPI_E_INTERFACE_NOT_SUPPORTED** , el cliente, a continuación, puede abrir **PR_ATTACH_DATA_BIN** con **IStream**. 
  
Si la aplicación cliente o el proveedor de servicios no se puede abrir un subobjetos datos adjuntos mediante el uso de **PR_ATTACH_DATA_OBJ** con la Ayuda de **PR_ATTACH_METHOD**, que debe usar **PR_ATTACH_DATA_BIN**. 
  
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
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

