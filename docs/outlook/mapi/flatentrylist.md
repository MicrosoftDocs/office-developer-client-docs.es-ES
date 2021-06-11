---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413860"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de [estructuras FLATENTRY.](flatentry.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Recuento de **estructuras FLATENTRY** en la matriz descrita por el **miembro abEntries.** 
    
**cbEntries**
  
> Recuento de bytes en la matriz descrita por **abEntries**. 
    
**abEntries**
  
> Matriz de bytes que contiene una o más estructuras **FLATENTRY,** dispuestas de extremo a extremo. 
    
## <a name="remarks"></a>Comentarios

En la **matriz abEntries,** cada **estructura FLATENTRY** se alinea en un límite alineado de forma natural. Se incluyen bytes adicionales como relleno para asegurarse de que la alineación natural entre las dos estructuras **FLATENTRY.** La primera **estructura FLATENTRY** de la matriz siempre se alinea correctamente porque el desplazamiento del **miembro abEntries** es 8. Para calcular el desplazamiento de la siguiente estructura, use el tamaño de la primera entrada redondeada hasta el múltiplo siguiente de 4. Use la [macro CbFLATENTRY](cbflatentry.md) para calcular el tamaño de una **estructura FLATENTRY.** 
  
Por ejemplo, la segunda estructura **FLATENTRY** comienza en un desplazamiento que consiste en el desplazamiento de la primera entrada más la longitud de la primera entrada redondeada a los cuatro bytes siguientes. La longitud de la primera entrada es la longitud de su **miembro cb** más la longitud de su **miembro abEntry.** 
  
El ejemplo de código siguiente indica cómo calcular desplazamientos en una **estructura FLATENTRYLIST.** Suponga que  _lpFlatEntry_ es un puntero a la primera estructura de la lista. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Vea también

- [FLATENTRY](flatentry.md)
- [Propiedad canónica PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Estructuras MAPI](mapi-structures.md)

