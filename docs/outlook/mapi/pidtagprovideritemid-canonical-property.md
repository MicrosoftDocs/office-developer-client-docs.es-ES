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
ms.openlocfilehash: 35a2d88ec838a9a76355ba6580e9cdbb3f28de56
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819989"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Propiedad canónica PidTagProviderItemId

  
  
**Hace referencia a**: Outlook 
  
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
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

