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
ms.openlocfilehash: e1846b4be93bf6300ea89a9ae3133fbba82b344e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573127"
---
# <a name="propid"></a>PROP_ID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el identificador de propiedad de una etiqueta de propiedad especificado.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Parámetros

 _ulPropTag_
  
> Etiqueta de la propiedad que contiene el identificador que se va a devolver.
    
## <a name="remarks"></a>Comentarios

Cada etiqueta de la propiedad contiene el tipo de propiedad de la palabra de orden inferior (bits del 0 al 15) y el identificador de propiedad de la palabra de orden superior (bits 16 a 31). La macro **PROP_ID** extrae el identificador de propiedad y la coloca en los bits 0 a 15 del número entero que se va a devolver. Se establecen los bits restantes del valor devuelto a ceros. 
  
La macro **PROP_ID** , por ejemplo, puede usarse para recuperar un identificador que se pase a [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). **GetNamesFromIDs** recupera el nombre de propiedad asociado con un identificador para una propiedad con nombre. 
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

