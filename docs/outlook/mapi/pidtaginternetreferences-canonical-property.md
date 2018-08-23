---
title: Propiedad canónica PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0e01d3f56ef01984f281e7fae5990ccb0eade88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593336"
---
# <a name="pidtaginternetreferences-canonical-property"></a>Propiedad canónica PidTagInternetReferences

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor del campo de encabezado de referencias de un mensaje de extensiones multipropósito de correo Internet (MIME).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W  <br/> |
|Identificador:  <br/> |0x1039  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Comentarios

Para generar un campo de encabezado de referencias, los clientes deben establecer estas propiedades en el valor deseado. Los escritores MIME deben copiar el valor de estas propiedades en el campo de encabezado de referencias.
  
Para establecer el valor de estas propiedades, los clientes MIME deben escribir el valor deseado en un campo de encabezado de referencias. Lectores MIME deben copiar el valor del campo de encabezado de referencias a estas propiedades. Lectores MIME pueden truncar el valor de estas propiedades si se excede 64KB de longitud.
  
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

