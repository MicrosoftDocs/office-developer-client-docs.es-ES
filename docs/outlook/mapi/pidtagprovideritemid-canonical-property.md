---
title: Propiedad canónica PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e0f13b0b8d2f7eb6fd7ba60e9e351b62251aa13d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572840"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Propiedad canónica PidTagProviderItemId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica un identificador para una carpeta o un elemento en un almacén.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_ITEMID  <br/> |
|Identificador:  <br/> |0x0EA3  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MapiNonTransmittable  <br/> |
   
## <a name="remarks"></a>Comentarios

Los proveedores de almacén pueden especificar un valor para esta propiedad para una carpeta o un elemento, pero deben mantener el valor de la misma entre sesiones. Los proveedores de almacén use esta propiedad para identificar los resultados de búsqueda devueltos por un motor de búsqueda.
  
## <a name="related-resources"></a>Recursos relacionados

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

