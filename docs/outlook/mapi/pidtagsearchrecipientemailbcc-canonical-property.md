---
title: Propiedad canónica PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359160"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>Propiedad canónica PidTagSearchRecipientEmailBcc

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena Unicode que se consulta en la lista de direcciones de correo electrónico o nombres para mostrar de los destinatarios que se abordan en la línea **CCO** de mensajes no enviados en el almacén. 
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|Identificador:  <br/> |0x0EA8  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Access:  <br/> |Búsqueda  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad solo es relevante para los mensajes del almacén que no se han enviado, ya que los mensajes que se han enviado o recibido no contienen información CCO.
  
> [!NOTE]
> Es posible que esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o nombres para mostrar a los que se enviará el mensaje como una copia de carbón ciego, no se defina en el archivo de encabezado descargable que tiene actualmente. Puede agregarlo al código mediante el siguiente valor: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

