---
title: Propiedad canónica PidTagSearchRecipientEmailTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358922"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a>Propiedad canónica PidTagSearchRecipientEmailTo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena Unicode que se consulta en la lista de direcciones de correo  electrónico o nombres para mostrar de los destinatarios que se abordan en la línea Para de los mensajes del almacén. 
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEARCH_RECIP_EMAIL_TO_W  <br/> |
|Identificador:  <br/> |0x0EA6  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Búsqueda  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

> [!NOTE]
> Es posible que esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o nombres para mostrar a los que se envía el mensaje, no esté definida en el archivo de encabezado descargable que tiene actualmente. Puedes agregarlo al código mediante el siguiente valor: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`
  
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
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

