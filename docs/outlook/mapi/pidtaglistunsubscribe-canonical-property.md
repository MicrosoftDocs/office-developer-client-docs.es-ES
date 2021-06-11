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
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278882"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>Propiedad canónica PidTagListUnsubscribe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor del campo de encabezado de un mensaje Multipurpose Internet Mail Extensions (MIME List-Unsubscribe).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W  <br/> |
|Identificador:  <br/> |0x1045  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Para generar un campo List-Unsubscribe encabezado, los clientes deben establecer estas propiedades en el valor deseado. Los escritores MIME deben copiar el valor de estas propiedades en el List-Unsubscribe de encabezado.
  
Para establecer el valor de estas propiedades relacionadas con el servidor de lista, los clientes MIME deben escribir los campos de encabezado como se especifica en la tabla siguiente.
  
|**Property**|**Nombre de campo de encabezado preferido**|**Nombre de campo de encabezado alternativo**|
|:-----|:-----|:-----|
|**PR_LIST_UNSUBSCRIBE** <br/> |List-Unsubscribe  <br/> |X-List-Unsubscribe  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
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

