---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282687"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [EntryID](entryid.md) con nombre que contiene un miembro **AB** de un tamaño especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parameters

__CB_
  
> Número de bytes en el miembro **AB** de la nueva estructura. 
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedENTRYID** permite definir un identificador de entrada después de conocer los requisitos de longitud de la matriz. Use esta macro para crear un identificador de entrada con límites explícitos. 
  
Para usar la nueva estructura que resulta de la macro **SizedENTRYID** como un puntero a una estructura **EntryID** , realice la siguiente conversión: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Vea también

- [ENTRYID](entryid.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

