---
title: Propiedad canónica PidTagSearchRecipientEmailCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 03501e14740d7b27bd54d761ae701e8863ad79dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358950"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a>Propiedad canónica PidTagSearchRecipientEmailCc

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena Unicode que se consulta en la lista de direcciones de correo electrónico o nombres para mostrar de los destinatarios que se abordan en la línea **CC** de mensajes en el almacén. 
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEARCH_RECIP_EMAIL_CC_W  <br/> |
|Identificador:  <br/> |0x0EA7  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Búsqueda  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

> [!NOTE]
> Es posible que esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o nombres para mostrar a los que se envía el mensaje como una copia de carbono, no se defina en el archivo de encabezado descargable que tiene actualmente. Puede agregarlo al código mediante el siguiente valor: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`
  
### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades que se enumeran como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

