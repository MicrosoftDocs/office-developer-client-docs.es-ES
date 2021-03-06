---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430703"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de etiquetas de propiedades. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de etiquetas de propiedad en la matriz indicada por el **miembro aulPropTag.** 
    
 **aulPropTag**
  
> Matriz de etiquetas de propiedad.
    
## <a name="remarks"></a>Comentarios

Una etiqueta de propiedad es un entero sin signo de 32 bits que consta de dos partes: 
  
- Un identificador en el orden alto de 16 bits.
    
- Tipo de 16 bits de orden bajo.
    
El identificador es un valor numérico en un intervalo determinado. MAPI define intervalos de identificadores para describir para qué se usa la propiedad y quién es responsable de mantenerla. MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags.h.
  
El tipo indica el formato del valor de la propiedad. MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs.h. 
  
Para obtener más información acerca de las etiquetas de propiedad y sus componentes, consulte uno de los siguientes temas: 
  
[Etiquetas de propiedad MAPI](mapi-property-tags.md)
  
[Información general del identificador de propiedad MAPI](mapi-property-identifier-overview.md)
  
[Información general del tipo de propiedad MAPI](mapi-property-type-overview.md)
  
Para obtener una lista completa de los tipos de propiedades de valor único y multivalor, vea el apéndice, [Identificadores](property-identifiers-and-types.md)de propiedad y Tipos . 
  
## <a name="see-also"></a>Vea también



[Estructuras MAPI](mapi-structures.md)

