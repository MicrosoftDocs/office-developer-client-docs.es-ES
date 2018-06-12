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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820764"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Se aplica a**: Outlook 
  
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

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpp** . 
    
 **lpp**
  
> Puntero a una matriz de valores enteros sin signo.
    
## <a name="remarks"></a>Notas

Para obtener más información acerca de PT_MV_SHORT y otros tipos de propiedades, vea [Tipos de propiedades](property-types.md). 
  
## <a name="see-also"></a>Ver también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

