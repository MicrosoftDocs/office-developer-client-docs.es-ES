---
title: Elemento SPropTagArray
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5cfad1c75aaab9afae47de5798f9e6b7ea530940
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820740"
---
# <a name="sproptagarray"></a>Elemento SPropTagArray

  
  
**Se aplica a**: Outlook 
  
Contiene una matriz de etiquetas de propiedad. 
  
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

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de etiquetas de propiedad en la matriz indicada por el miembro **aulPropTag** . 
    
 **aulPropTag**
  
> Matriz de las etiquetas de propiedad.
    
## <a name="remarks"></a>Notas

Una etiqueta de propiedad es un entero sin signo de 32 bits que consta de dos partes: 
  
- Un identificador de orden superior a 16 bits.
    
- Un tipo de orden inferior a 16 bits.
    
El identificador es un valor numérico en un intervalo determinado. MAPI define los intervalos para los identificadores describir la propiedad que se usa para y quién es responsable de mantenerlo. MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags.h.
  
El tipo indica el formato para el valor de la propiedad. MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs.h. 
  
Para obtener más información acerca de las etiquetas de propiedad y sus componentes, vea uno de los siguientes temas: 
  
[Etiquetas MAPI (propiedad)](mapi-property-tags.md)
  
[Información general sobre el identificador de propiedad MAPI](mapi-property-identifier-overview.md)
  
[Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md)
  
Para obtener una lista completa de los tipos de propiedad de valor único y de varios valores, consulte el apéndice, [identificadores de propiedades y tipos](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>Ver también



[Estructuras MAPI](mapi-structures.md)

