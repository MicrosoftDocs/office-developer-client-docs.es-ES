---
title: Propiedad canónica PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387212"
---
# <a name="pidtaglisthelp-canonical-property"></a>Propiedad canónica PidTagListHelp

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor del campo de encabezado de Ayuda de la lista de un mensaje de extensiones multipropósito de correo Internet (MIME).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W  <br/> |
|Identificador:  <br/> |0x1043  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Para generar un campo de encabezado de Ayuda de la lista, los clientes deben establecer el valor de **PR_LIST_HELP** o una propiedad asociada en el valor deseado. Los escritores MIME deben copiar este valor en el campo de encabezado de Ayuda de la lista. 
  
Para establecer el valor de estas propiedades relacionadas con el servidor de lista, los clientes MIME deben escribir los campos de encabezado tal como se especifica en la siguiente tabla:
  
|**Propiedad**|**Nombre de campo de encabezado preferido**|**Nombre de campo de encabezado alternativo**|
|:-----|:-----|:-----|
|**PR_LIST_HELP** <br/> |Ayuda de la lista  <br/> |X-lista-Help  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

