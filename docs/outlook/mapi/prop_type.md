---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412838"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el tipo de propiedad de una etiqueta de propiedad especificada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> Etiqueta de propiedad que contiene el tipo de propiedad que se va a devolver.
    
## <a name="remarks"></a>Comentarios

La macro **PROP_TYPE** se puede usar para determinar el tipo de una propiedad. Por ejemplo, llamar a PROP_TYPE**** (método ([PidTagEntryId](pidtagentryid-canonical-property.md))) da como resultado el valor PT_BINARY que se devuelve.
  
Cada etiqueta de propiedad contiene el tipo de propiedad en la palabra de orden inferior (bits del 0 al 15) y el identificador de la propiedad en la palabra de orden superior (bits 16 a 31). La macro **PROP_TYPE** extrae el tipo de propiedad y lo coloca en los bits del 0 al 15 del entero que se va a devolver. Los bits restantes del valor devuelto se establecen en ceros. 
  
## <a name="see-also"></a>Ver también



[SPropValue](spropvalue.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

