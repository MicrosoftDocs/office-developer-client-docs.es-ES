---
title: Propiedad canónico PidLidCategories
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818594"
---
# <a name="pidlidcategories-canonical-property"></a>Propiedad canónico PidLidCategories

  
  
**Se aplica a**: Outlook 
  
Especifica una lista de categorías para un elemento.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidCategories  <br/> |
|Conjunto de propiedades:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00002328  <br/> |
|Tipo de datos:  <br/> |PT_MV_UNICODE  <br/> |
|Área:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Notas

Para generar un campo de encabezado de palabras clave, los clientes deben establecer el valor de esta propiedad en los valores deseados. Esta propiedad tiene varias cadenas; cada categoría se debe asignar a una palabra clave única.
  
Extensiones multipropósito escritores de extensiones de correo Internet (MIME) deben copiar cada valor subcaracterística de esta propiedad para una palabra clave independiente en el campo de encabezado de palabras clave, con una coma (U + 002 C) y espacio (u+0020) separando cada palabra clave. Los escritores MIME pueden colocar esta propiedad en lugar de copiarlo en el campo de encabezado de palabras clave, con el fin de evitar conflictos entre distintos conjuntos de categorías de distintas organizaciones.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

