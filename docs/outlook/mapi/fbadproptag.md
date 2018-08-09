---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816793"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Hace referencia a**: Outlook 
  
Valida una etiqueta de propiedad especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parámetros

 _ulPropTag_
  
> [entrada] La etiqueta de propiedad que se va a validar.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La etiqueta de propiedad especificado no es una etiqueta de propiedad MAPI válida. 
    
FALSE 
  
> La etiqueta de la propiedad especificada es una etiqueta de propiedad MAPI válida.
    
## <a name="remarks"></a>Comentarios

La función **FBadPropTag** valida la etiqueta de propiedad especificado en función de las definiciones de MAPI. Asegúrese de que el tipo de propiedad es uno de los tipos definidos por MAPI y que se define el identificador de la propiedad para que sea de ese tipo de sures. 
  
## <a name="see-also"></a>Vea también



[FBadProp](fbadprop.md)

