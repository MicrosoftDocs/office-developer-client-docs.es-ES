---
title: Propiedad canónica PidTagAttachMethod
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Última modificación: 07 de septiembre de 2016'
ms.openlocfilehash: 697f7e8045ca198c2c10b9396f19cb2d7ce8346e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583655"
---
# <a name="pidtagattachmethod-canonical-property"></a>Propiedad canónica PidTagAttachMethod

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una constante definidas en MAPI que representa la manera en que se puede tener acceso el contenido de los datos adjuntos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_METHOD  <br/> |
|Identificador:  <br/> |0x3705  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener exactamente uno de los siguientes valores:
  
NO_ATTACHMENT 
  
> Los datos adjuntos se acaba de crear. 
    
ATTACH_BY_VALUE 
  
> La propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contiene los datos adjuntos. 
    
ATTACH_BY_REFERENCE 
  
> La propiedad de **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) o **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) contiene una ruta de acceso completo que identifica los datos adjuntos a los destinatarios con acceso a un archivo común servidor. 
    
ATTACH_BY_REF_RESOLVE 
  
> La propiedad **PR_ATTACH_PATHNAME** o **PR_ATTACH_LONG_PATHNAME** contiene una ruta de acceso completo que identifica los datos adjuntos. 
    
ATTACH_BY_REF_ONLY 
  
> La propiedad **PR_ATTACH_PATHNAME** o **PR_ATTACH_LONG_PATHNAME** contiene una ruta de acceso completo que identifica los datos adjuntos. 
    
ATTACH_EMBEDDED_MSG 
  
> La propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contiene un objeto incrustado que admite **la interfaz** . 
    
ATTACH_OLE 
  
> Los datos adjuntos son un objeto OLE incrustado.
    
ATTACH_BY_WEBREFERENCE 
  
> El contenido de los datos adjuntos no está en el mensaje. 
    
Cuando se crean, todos los objetos de datos adjuntos tienen un valor inicial de **PR_ATTACH_METHOD** de **NO_ATTACHMENT**. 
  
Aplicaciones cliente y los proveedores de servicios sólo son necesarios para admitir el método de datos adjuntos representado por el valor **ATTACH_BY_VALUE** . Los otros métodos de datos adjuntos son opcionales. El almacén de mensajes no aplicar cualquier coherencia entre el valor de **PR_ATTACH_METHOD** y los valores de las demás propiedades de los datos adjuntos. 
  
Se recomiendan nombres (UNC) de la convención de nomenclatura universal para rutas de acceso completas, que se deben usar con **ATTACH_BY_REFERENCE** y **ATTACH_BY_REF_ONLY**. Con **ATTACH_BY_REF_RESOLVE**, una ruta de acceso absoluta es más rápido, debido a que la cola MAPI convierte **ATTACH_BY_VALUE**de los datos adjuntos. 
  
Si se establece **ATTACH_BY_REFERENCE** , **PR_ATTACH_DATA_BIN** debe estar vacío. Una puerta de enlace saliente puede activar **ATTACH_BY_REFERENCE** adjuntos en datos adjuntos **ATTACH_BY_VALUE** copiando los datos adjuntos en la propiedad **PR_ATTACH_DATA_BIN** . 
  
Si se establece **ATTACH_BY_REF_RESOLVE** , **PR_ATTACH_DATA_BIN** debe estar vacío. Cuando se envía el mensaje que contiene los datos adjuntos de **ATTACH_BY_REF_RESOLVE** , la cola MAPI copia los datos adjuntos en un archivo adjunto de **ATTACH_BY_VALUE** . Este proceso de resolución coloca los datos adjuntos en **PR_ATTACH_DATA_BIN**. 
  
Si se establece **ATTACH_BY_REF_ONLY** , **PR_ATTACH_DATA_BIN** debe estar vacío, y el sistema de mensajería nunca resuelve la referencia de datos adjuntos. Utilice este valor cuando desea enviar el vínculo, pero no los datos. 
  
Cuando el objeto OLE está en formato de OLE 2.0 **IStorage** , los datos están accesibles a través de **PR_ATTACH_DATA_OBJ**. Cuando el objeto OLE está en formato OLE 1.0 **OLESTREAM** , los datos están accesibles a través de **PR_ATTACH_DATA_BIN** como **IStream**. El tipo de la codificación de OLE puede ser determinado por el valor de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para obtener más información sobre las interfaces OLE y formatos, vea la *referencia del programador de OLE* . 
  
## <a name="remarks"></a>Comentarios

Cuando el **PR_ATTACH_METHOD** es **ATTACH_BY_WEBREFERENCE**, el contenido de los datos adjuntos no está en el mensaje. En su lugar, la propiedad **PR_ATTACH_LONG_FILENAME** contiene una dirección URL absoluta para el contenido de datos adjuntos, que esté almacenado en línea. 
  
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



[Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

