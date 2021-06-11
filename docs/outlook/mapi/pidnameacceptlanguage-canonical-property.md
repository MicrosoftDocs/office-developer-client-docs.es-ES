---
title: Propiedad canónica PidNameAcceptLanguage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360945"
---
# <a name="pidnameacceptlanguage-canonical-property"></a>Propiedad canónica PidNameAcceptLanguage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor de campo de encabezado Accept-Language [RFC3282].
  
|||
|:-----|:-----|
|Nombres descriptivos:  <br/> |AcceptLanguage  <br/> |
|Conjunto de propiedades:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nombre de la propiedad:  <br/> |Accept-Language  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer el valor de esta propiedad, los clientes de Multipurpose Internet Message Extensions (MIME) deben escribir un campo Accept-Language encabezado con el valor deseado. En su lugar, los clientes MIME pueden escribir un campo de encabezado X-Accept-Language. Los lectores MIME deben copiar el valor de cualquier campo de encabezado en el valor de esta propiedad. Si ambos campos de encabezado están presentes, los lectores MIME deben usar el Accept-Language de encabezado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

