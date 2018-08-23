---
title: Propiedad canónica PidTagListUnsubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1a4011a22f1029cc4002d4506eb4d335bd280bec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593441"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>Propiedad canónica PidTagListUnsubscribe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor del campo de encabezado de un mensaje de extensiones multipropósito de correo Internet (MIME) cancelar su suscripción de lista.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W  <br/> |
|Identificador:  <br/> |0x1045  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Para generar un campo de encabezado cancelar su suscripción de lista, los clientes deben establecer estas propiedades en el valor deseado. Los escritores MIME deben copiar el valor de estas propiedades en el campo de encabezado de cancelar su suscripción de lista.
  
Para establecer el valor de estas propiedades relacionadas con el servidor de lista, los clientes MIME deben escribir los campos de encabezado tal como se especifica en la siguiente tabla.
  
|**Propiedad**|**Nombre de campo de encabezado preferido**|**Nombre de campo de encabezado alternativo**|
|:-----|:-----|:-----|
|**PR_LIST_UNSUBSCRIBE** <br/> |Cancelar su suscripción de lista  <br/> |Anular la suscripción X-lista  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

