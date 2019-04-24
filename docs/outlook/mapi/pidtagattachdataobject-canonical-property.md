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
  
Contiene un objeto Attachment al que se tiene acceso normalmente a través de la interfaz **IStorage** de vinculación e incrustaCión de objetos (OLE). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es **ATTACH_EMBEDDED_MSG** o **ATTACH_OLE**. El tipo de codificación OLE se puede determinar a partir de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para los datos adjuntos asociados con el valor **ATTACH_EMBEDDED_MSG** , se puede usar la interfaz [IMessage: IMAPIProp](imessageimapiprop.md) para un acceso más rápido. 
  
Para un objeto OLE dinámico incrustado, la propiedad **PR_ATTACH_DATA_OBJ** contiene su propia información de representación y la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) debe ser inexistente o estar vacía. 
  
Para un archivo adjunto de documento OLE, el proveedor de almacenamiento de mensajes debe responder a una llamada de [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) en **PR_ATTACH_DATA_OBJ** y, opcionalmente, responder a una llamada en **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ). Las propiedades **PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** comparten el mismo identificador de propiedad y, por tanto, son dos representaciones de la misma propiedad. 
  
Para un objeto de almacenamiento, como un archivo compuesto en el formato OLE 2,0 de archivos de almacenamiento, algunos proveedores de servicios permiten que se abra con la interfaz MAPI **IStreamDocfile** , una subclase de **IStream** sin miembros adicionales, diseñada para optimizar el rendimiento. El posible ahorro es suficiente para justificar el intento de abrir **PR_ATTACH_DATA_OBJ** a través de **IStreamDocfile**. Si se devuelve **MAPI_E_INTERFACE_NOT_SUPPORTED** , el cliente puede abrir **PR_ATTACH_DATA_BIN** con **IStream**. 
  
Si la aplicación cliente o el proveedor de servicios no puede abrir un objeto Attachment mediante **PR_ATTACH_DATA_OBJ** con la ayuda de **PR_ATTACH_METHOD**, debe usar **PR_ATTACH_DATA_BIN**. 
  
Para obtener más información sobre los formatos y las interfaces OLE, consulte [OLE y transferencia de datos](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
## <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

