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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405712"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [ENTRYID](entryid.md) con nombre que contiene un **miembro ab** de un tamaño especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parámetros

_ _cb_
  
> Número de bytes en el **miembro ab** de la nueva estructura. 
    
_ _name_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La **macro SizedENTRYID** permite definir un identificador de entrada después de conocer los requisitos de longitud de la matriz. Use esta macro para crear un identificador de entrada con límites explícitos. 
  
Para usar la nueva estructura que resulta de la macro **SizedENTRYID** como puntero a una estructura **ENTRYID,** realice la conversión siguiente: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Consulte también

- [ENTRYID](entryid.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

