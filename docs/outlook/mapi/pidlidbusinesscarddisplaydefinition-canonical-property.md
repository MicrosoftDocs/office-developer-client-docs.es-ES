---
title: Propiedad canónica PidLidBusinessCardDisplayDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342038"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>Propiedad canónica PidLidBusinessCardDisplayDefinition

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene los detalles de personalización del usuario para mostrar un contacto como una tarjeta de presentación.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidBCDisplayDefinition  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008040  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

El diseño de una tarjeta de presentación se puede representar como una imagen y varios campos de texto. La imagen puede ser una foto de contacto o una imagen de tarjeta. Los campos de texto constan de un valor de otra propiedad establecida en el contacto y una cadena de etiqueta personalizada opcional proporcionada por el usuario. Ten en cuenta que los valores de varios bytes se almacenan en formato little-endian en el búfer.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

