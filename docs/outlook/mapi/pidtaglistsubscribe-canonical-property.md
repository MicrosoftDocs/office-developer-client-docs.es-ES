---
title: Propiedad canónica PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279660"
---
# <a name="pidtaglistsubscribe-canonical-property"></a>Propiedad canónica PidTagListSubscribe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor de un campo de encabezado de suscripción de lista-suscripción del mensaje de extensiones de correo de Internet multipropósito (MIME).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W  <br/> |
|Identificador:  <br/> |0x1044  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Para generar un campo de encabezado List-subscribe, los clientes deben establecer el valor de estas propiedades en el valor deseado. Los escritores MIME deben copiar el valor de estas propiedades en el campo de encabezado List-subscribe.
  
Para establecer el valor de las propiedades relacionadas con el servidor de este modo, los clientes MIME deben escribir los campos de encabezado como se especifica en la siguiente tabla.
  
|**Property**|**Nombre de campo de encabezado preferido**|**Nombre de campo de encabezado alternativo**|
|:-----|:-----|:-----|
|**PidTagListSubscribe** <br/> |List-subscribe  <br/> |X-List-subscribe  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

