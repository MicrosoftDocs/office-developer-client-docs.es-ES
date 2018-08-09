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
ms.openlocfilehash: 814cfeab61854469f460cc38f927b0e3723f6f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820680"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Hace referencia a**: Outlook 
  
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

## <a name="see-also"></a>Vea también

- [ENTRYID](entryid.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

