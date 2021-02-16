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
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339287"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Propiedad canónica PidTagAttachDataObject

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un objeto adjunto al que normalmente se tiene acceso a través de la interfaz **IStorage** de vinculación e incrustación de objetos (OLE). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de datos:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es **ATTACH_EMBEDDED_MSG** o **ATTACH_OLE**. El tipo de codificación OLE se puede determinar **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para los datos adjuntos asociados **ATTACH_EMBEDDED_MSG** valor, la [interfaz IMessage:IMAPIProp](imessageimapiprop.md) se puede usar para un acceso más rápido. 
  
Para un objeto OLE dinámico incrustado, la propiedad **PR_ATTACH_DATA_OBJ** contiene su propia información de representación y la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) debe ser inexistente o vacía. 
  
Para los datos adjuntos de un archivo de documento OLE, el proveedor del almacén de mensajes debe responder **a** una llamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en PR_ATTACH_DATA_OBJ y, opcionalmente, puede responder a una llamada en **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). Las **PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** comparten el mismo identificador de propiedad y, por lo tanto, son dos representaciones de la misma propiedad. 
  
Para un objeto de almacenamiento, como un archivo compuesto en formato docfile OLE 2.0, algunos proveedores de servicios permiten que se abra con la interfaz **MAPI IStreamDocfile,** una subclase de **IStream** sin miembros adicionales, diseñada para optimizar el rendimiento. El posible almacenamiento es suficiente para justificar el intento de abrir **PR_ATTACH_DATA_OBJ** a través **de IStreamDocfile**. Si **MAPI_E_INTERFACE_NOT_SUPPORTED** se devuelve, el cliente puede abrir **PR_ATTACH_DATA_BIN** con **IStream**. 
  
Si la aplicación cliente o el proveedor de servicios no pueden abrir un subobjeto de datos adjuntos mediante **PR_ATTACH_DATA_OBJ** con la ayuda de **PR_ATTACH_METHOD**, debe usar **PR_ATTACH_DATA_BIN**. 
  
Para obtener más información sobre las interfaces y formatos OLE, vea [OLE y transferencia de datos.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
## <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

