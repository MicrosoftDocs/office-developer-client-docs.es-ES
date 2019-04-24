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
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341002"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una etiqueta de propiedad especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parámetros

 _ulPropTag_
  
> a Etiqueta de propiedad que se va a validar.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La etiqueta de propiedad especificada no es una etiqueta de propiedad MAPI válida. 
    
FALSE 
  
> La etiqueta de propiedad especificada es una etiqueta de propiedad MAPI válida.
    
## <a name="remarks"></a>Comentarios

La función **FBadPropTag** valida la etiqueta de propiedad especificada basándose en las definiciones de MAPI. Asegura que el tipo de propiedad es uno de los tipos definidos por MAPI y que el identificador de la propiedad se define para que sea de ese tipo. 
  
## <a name="see-also"></a>Vea también



[FBadProp](fbadprop.md)

