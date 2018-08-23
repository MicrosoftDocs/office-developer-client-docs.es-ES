---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573036"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de entero sin signo que se utilizan para describir una propiedad de tipo PT_MV_SHORT.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpp** . 
    
 **lpp**
  
> Puntero a una matriz de valores enteros sin signo.
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de PT_MV_SHORT y otros tipos de propiedades, vea [Tipos de propiedades](property-types.md). 
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

