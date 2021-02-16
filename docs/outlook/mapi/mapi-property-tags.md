---
title: Etiquetas de propiedad MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328245"
---
# <a name="mapi-property-tags"></a>Etiquetas de propiedad MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una etiqueta de propiedad es un número de 32 bits que contiene un identificador de propiedad único en los bits 16 a 31 y un tipo de propiedad en bits del 0 al 15, como se muestra en la siguiente ilustración. 
  
**Elementos de etiqueta de propiedad**
  
![Elementos de etiqueta de propiedad Elementos]de etiqueta de(media/amapi_10.gif "propiedad")
  
Las etiquetas de propiedad se usan para identificar propiedades MAPI y cada propiedad debe tener una, independientemente de si la propiedad está definida por MAPI, un cliente o un proveedor de servicios. MAPI define un conjunto de constantes de etiqueta de propiedad para sus propiedades en el archivo de encabezado Mapitags.h; Estas propiedades se denominan "propiedades definidas por MAPI". 
  
Las constantes de etiqueta de propiedad siguen una convención de nomenclatura para mantener la coherencia y la facilidad de uso. Hay dos partes en el nombre de cada etiqueta de propiedad: un prefijo PR_ y una o más cadenas de caracteres que describen el contenido de la propiedad. Las cadenas de varios caracteres están separadas por caracteres de subrayado. Por ejemplo, la etiqueta de propiedad para el tipo de dirección de un destinatario de mensaje es **PR \_ ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) y el identificador de entrada de la carpeta designada para recibir una copia de cada mensaje saliente es **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Hay algunas macros disponibles para ayudar a trabajar con etiquetas de propiedad, entre ellas [PROP_TYPE,](prop_type.md) [PROP_ID](prop_id.md)y [PROP_TAG](prop_tag.md). **PROP \_ TYPE** extrae el tipo de propiedad de la etiqueta de propiedad; **PROP \_ Id.** extrae el identificador. **PROP_TAG** genera una etiqueta de propiedad a partir de un identificador y un tipo de propiedad. 
  
## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)

