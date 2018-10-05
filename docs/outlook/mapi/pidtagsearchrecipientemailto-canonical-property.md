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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382620"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a>Propiedad canónica PidTagSearchRecipientEmailTo

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena Unicode que se está realizando la consulta en la lista de direcciones de correo electrónico o nombres para mostrar de los destinatarios que se tratan en la línea **para** de los mensajes en el almacén. 
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEARCH_RECIP_EMAIL_TO_W  <br/> |
|Identificador:  <br/> |0x0EA6  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Búsqueda  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

> [!NOTE]
> Esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o mostrar nombres al que se envía el mensaje, no puede definirse en el archivo de encabezado descargables que tiene actualmente. Puede agregar a su código con el siguiente valor: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`
  
### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
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

