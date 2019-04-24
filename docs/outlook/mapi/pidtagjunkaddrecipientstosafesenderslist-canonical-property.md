---
title: Propiedad canónica PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282371"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Propiedad canónica PidTagJunkAddRecipientsToSafeSendersList

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si los destinatarios de correo se van a agregar a la lista de remitentes seguros.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Identificador:  <br/> |0x6103  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Correo no deseado  <br/> |
   
## <a name="remarks"></a>Comentarios

Si está presente, esta propiedad debe establecerse en 0 o 1. Un valor de 1 indica que los destinatarios de correo se agregarán a la lista de remitentes seguros. Un valor de 0 indica que los destinatarios de correo no se van a agregar a la lista de remitentes seguros.
  
Si esta propiedad está presente con un valor de 1, las direcciones SMTP de los destinatarios de correo electrónico deben agregarse a la cláusula de remitentes de confianza de la condición de regla de correo electrónico no deseado. Si esta propiedad es 0, no se requiere ninguna acción.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.
    
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

