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
ms.openlocfilehash: d797acdbf2abfb88151d69d0c93e743f07afc5c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563873"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [ENTRYID](entryid.md) con nombre que contiene a un miembro **ab** de un tamaño especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parámetros

__cb_
  
> Recuento de bytes en el miembro **ab** de la nueva estructura. 
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedENTRYID** le permite definir un identificador de entrada después de que se conocen los requisitos de longitud de la matriz. Use esta macro para crear un identificador de entrada con límites explícitos. 
  
Para usar la nueva estructura que el resultado de la macro **SizedENTRYID** como un puntero a una estructura de la **propiedad ENTRYID** , realice la conversión de tipos siguiente: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Recursos adicionales

- [ENTRYID](entryid.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

