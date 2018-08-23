---
title: Etiquetas MAPI (propiedad)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 314d2d6987a8bc669239652b83a31b5927723c68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562928"
---
# <a name="mapi-property-tags"></a>Etiquetas MAPI (propiedad)
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una etiqueta de propiedad es un número de 32 bits que contiene un identificador de propiedad único de 31 a 16 bits y un tipo de propiedad en los bits 0 a 15, tal como se muestra en la siguiente ilustración. 
  
**Elementos de etiqueta de propiedad**
  
![Elementos de etiqueta (propiedad)] (media/amapi_10.gif "Elementos de etiqueta (propiedad)")
  
Etiquetas de propiedad se usan para identificar las propiedades MAPI y cada propiedad debe tener uno, independientemente de si se ha definido la propiedad MAPI, un cliente o un proveedor de servicios. MAPI define un conjunto de constantes de etiqueta de propiedad de sus propiedades en el archivo de encabezado Mapitags.h; Estas propiedades se conocen como "propiedades definidas por el MAPI". 
  
Las constantes de etiqueta de propiedad siguen una convención de nomenclatura para coherencia y facilidad de uso. Hay dos partes en el nombre de cada etiqueta de la propiedad: un prefijo PR_ y uno o más cadenas de caracteres que describen el contenido de la propiedad. Varias cadenas de caracteres están separadas por caracteres de subrayado. Por ejemplo, la etiqueta de propiedad para el tipo de dirección de destinatario de un mensaje es **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) y el identificador de entrada de la carpeta designada para recibir una copia de cada mensaje saliente es **PR_IPM_SENTMAIL_ Propiedad ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Algunas macros están disponibles para ayudar a trabajar con etiquetas de propiedad, entre ellas, [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)y [PROP_TAG](prop_tag.md). **PROPIEDADES\_tipo** extrae el tipo de propiedad de la etiqueta de propiedad; **Propiedades\_identificador** extrae el identificador. **PROP_TAG** genera una etiqueta de propiedad de un tipo de propiedad y un identificador. 
  
## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)

