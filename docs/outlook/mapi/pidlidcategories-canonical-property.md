---
title: Propiedad canónica PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344978"
---
# <a name="pidlidcategories-canonical-property"></a>Propiedad canónica PidLidCategories

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica una lista de categorías para un elemento.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidCategories  <br/> |
|Conjunto de propiedades:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Long ID (LID):  <br/> |0x00002328  <br/> |
|Tipo de datos:  <br/> |PT_MV_UNICODE  <br/> |
|Área:  <br/> |Común  <br/> |
   
## <a name="remarks"></a>Comentarios

Para generar un campo de encabezado de palabras clave, los clientes deben establecer el valor de esta propiedad en los valores deseados. Esta propiedad tiene varias cadenas; cada categoría debe asignarse a una sola palabra clave.
  
Los escritores multipropósito a extensiones de correo de Internet (MIME) deben copiar cada subínclave de esta propiedad en una palabra clave independiente en el campo de encabezado Palabras clave, con una coma (U+002C) y un espacio (U+0020) que separe cada palabra clave. Los escritores mime pueden colocar esta propiedad en lugar de copiarla en el campo de encabezado de palabras clave, para evitar conflictos entre distintos conjuntos de categorías en diferentes organizaciones.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona la definición del conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

