---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328577"
---
# <a name="propid"></a>PROP_ID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el identificador de la propiedad de una etiqueta de propiedad especificada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> Etiqueta de propiedad que contiene el identificador que se va a devolver.
    
## <a name="remarks"></a>Comentarios

Cada etiqueta de propiedad contiene el tipo de propiedad en la palabra de orden inferior (bits del 0 al 15) y el identificador de la propiedad en la palabra de orden superior (bits 16 a 31). La macro **PROP_ID** extrae el identificador de la propiedad y lo coloca en los bits del 0 al 15 del entero que se va a devolver. Los bits restantes del valor devuelto se establecen en ceros. 
  
Se puede usar la macro **PROP_ID** , por ejemplo, para recuperar un identificador para pasar a [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md). **GetNamesFromIDs** recupera el nombre de propiedad asociado a un identificador para una propiedad con nombre. 
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

