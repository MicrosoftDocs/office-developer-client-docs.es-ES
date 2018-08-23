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
ms.openlocfilehash: 6a3d0d79d190b318d36fd9be8a3ec39d6aa7ad29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593980"
---
# <a name="mviprop"></a>MVI_PROP

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el MVI_FLAG para una propiedad especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parámetros

 _etiqueta_
  
> La etiqueta de propiedad que desea modificar.
    
## <a name="remarks"></a>Comentarios

El MVI_FLAG se combina la configuración de MV_FLAG, que identifica una propiedad como multivalor y MV_INSTANCE, que solicita que se muestre una propiedad con varios valores en una tabla en varias filas. Se modifica el tipo de propiedad de la propiedad afectado, pero el identificador permanece inalterado. 
  
Por ejemplo, cuando la macro MVI_PROP se aplica a una propiedad de tipo PT_FLOAT, su tipo se cambia a PT_MV_FLOAT. Cuando se incluye en una tabla, se usan varias filas para representar la propiedad que tiene una fila para cada valor. Las propiedades de las demás columnas se repiten. 
  
Para obtener más información acerca de estos indicadores, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y [trabajar con columnas con varios valores](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

