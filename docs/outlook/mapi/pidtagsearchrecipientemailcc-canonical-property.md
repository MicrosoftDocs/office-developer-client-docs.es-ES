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
ms.openlocfilehash: 6fe59bf837d6123e5655e853531d6ab53393af91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820256"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a>Propiedad canónica PidTagSearchRecipientEmailCc

  
  
**Hace referencia a**: Outlook 
  
Contiene una cadena Unicode que se está realizando la consulta en la lista de direcciones de correo electrónico o nombres para mostrar de los destinatarios que se tratan en la línea **CC** de los mensajes en el almacén. 
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEARCH_RECIP_EMAIL_CC_W  <br/> |
|Identificador:  <br/> |0x0EA7  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Búsqueda  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

> [!NOTE]
> Esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o mostrar nombres al que se envía el mensaje como una copia, no puede definirse en el archivo de encabezado descargables que tiene actualmente. Puede agregar a su código con el siguiente valor: >`#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`
  
### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que se muestran como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

