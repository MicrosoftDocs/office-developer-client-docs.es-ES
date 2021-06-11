---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410682"
---
# <a name="mvi_prop"></a>MVI_PROP

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el MVI_FLAG para una propiedad especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parameters

 _etiqueta_
  
> Etiqueta de propiedad que se va a modificar.
    
## <a name="remarks"></a>Comentarios

El MVI_FLAG combina la configuración de MV_FLAG, identificando una propiedad como multivalor y MV_INSTANCE, solicitando que una propiedad de varios valores se muestre en una tabla en varias filas. El tipo de propiedad de la propiedad afectada se modifica, pero el identificador permanece sin cambios. 
  
Por ejemplo, cuando la macro MVI_PROP se aplica a una propiedad de tipo PT_FLOAT, su tipo se cambia a PT_MV_FLOAT. Cuando se incluye en una tabla, se usan varias filas para representar la propiedad que tiene una fila por cada valor. Las propiedades de las otras columnas se repiten. 
  
Para obtener más información acerca de estas marcas, vea Información general sobre el tipo de propiedad [MAPI](mapi-property-type-overview.md) y [Trabajar con columnas multivalor](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

