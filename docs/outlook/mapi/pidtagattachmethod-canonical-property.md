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
description: 'Last modified: September 07, 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327261"
---
# <a name="pidtagattachmethod-canonical-property"></a>Propiedad canónica PidTagAttachMethod

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una constante definida por MAPI que representa la forma en que se puede tener acceso al contenido de los datos adjuntos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_METHOD  <br/> |
|Identificador:  <br/> |0x3705  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener exactamente uno de los siguientes valores:
  
NO_ATTACHMENT 
  
> Los datos adjuntos se han creado. 
    
ATTACH_BY_VALUE 
  
> La **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contiene los datos adjuntos. 
    
ATTACH_BY_REFERENCE 
  
> La **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) o **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) contiene una ruta de acceso completa que identifica los datos adjuntos a los destinatarios con acceso a un servidor de archivos común. 
    
ATTACH_BY_REF_RESOLVE 
  
> La **PR_ATTACH_PATHNAME** o **PR_ATTACH_LONG_PATHNAME** contiene una ruta de acceso completa que identifica los datos adjuntos. 
    
ATTACH_BY_REF_ONLY 
  
> La **PR_ATTACH_PATHNAME** o **PR_ATTACH_LONG_PATHNAME** contiene una ruta de acceso completa que identifica los datos adjuntos. 
    
ATTACH_EMBEDDED_MSG 
  
> La **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contiene un objeto incrustado que admite la **interfaz IMessage.** 
    
ATTACH_OLE 
  
> Los datos adjuntos son un objeto OLE incrustado.
    
ATTACH_BY_WEBREFERENCE 
  
> El contenido de los datos adjuntos no está en el mensaje. 
    
Cuando se crean, todos los objetos adjuntos tienen un **valor PR_ATTACH_METHOD** inicial de **NO_ATTACHMENT**. 
  
Las aplicaciones cliente y los proveedores de servicios solo son necesarios para admitir el método de datos adjuntos representado por **el ATTACH_BY_VALUE** cliente. Los otros métodos de datos adjuntos son opcionales. El almacén de mensajes no exige ninguna coherencia entre el valor de **PR_ATTACH_METHOD** y los valores de las otras propiedades de datos adjuntos. 
  
Se recomiendan nombres de convención de nomenclatura universal (UNC)  para rutas de acceso completas, que se deben usar con ATTACH_BY_REFERENCE **y ATTACH_BY_REF_ONLY**. Con **ATTACH_BY_REF_RESOLVE,** una ruta de acceso absoluta es más rápida, porque la cola MAPI convierte los datos adjuntos en **ATTACH_BY_VALUE**. 
  
Si **ATTACH_BY_REFERENCE** está establecido, **PR_ATTACH_DATA_BIN** debe estar vacío. Una puerta de enlace saliente puede convertir ATTACH_BY_REFERENCE **datos** adjuntos en un ATTACH_BY_VALUE **adjuntos** copiando los datos adjuntos en la **PR_ATTACH_DATA_BIN** datos adjuntos. 
  
Si **ATTACH_BY_REF_RESOLVE** se establece, **PR_ATTACH_DATA_BIN** debe estar vacío. Cuando se envía el mensaje que ATTACH_BY_REF_RESOLVE **datos** adjuntos, la cola MAPI copia los datos adjuntos **en** una ATTACH_BY_VALUE datos adjuntos. Este proceso de resolución coloca los datos adjuntos **en PR_ATTACH_DATA_BIN**. 
  
Si **ATTACH_BY_REF_ONLY** se establece, **PR_ATTACH_DATA_BIN** debe estar vacío y el sistema de mensajería nunca resuelve la referencia de datos adjuntos. Use este valor cuando desee enviar el vínculo, pero no los datos. 
  
Cuando el objeto OLE está en formato **IStorage** de OLE 2.0, se puede acceder a los datos a través **de PR_ATTACH_DATA_OBJ**. Cuando el objeto OLE está en formato OLE 1.0 **OLESTREAM,** los datos son accesibles a través **PR_ATTACH_DATA_BIN** como **un IStream**. El tipo de la codificación OLE puede determinarse mediante **el PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para obtener más información sobre las interfaces y formatos OLE, vea la referencia *del programador de OLE.* 
  
## <a name="remarks"></a>Comentarios

Cuando el **PR_ATTACH_METHOD** está **ATTACH_BY_WEBREFERENCE,** el contenido de los datos adjuntos no está en el mensaje. En su lugar, **PR_ATTACH_LONG_FILENAME** propiedad contiene una dirección URL absoluta para el contenido de datos adjuntos, que se almacena en línea. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

