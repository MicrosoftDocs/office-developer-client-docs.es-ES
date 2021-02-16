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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433650"
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
  
> [entrada] Etiqueta de propiedad que se va a validar.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La etiqueta de propiedad especificada no es una etiqueta de propiedad MAPI válida. 
    
FALSE 
  
> La etiqueta de propiedad especificada es una etiqueta de propiedad MAPI válida.
    
## <a name="remarks"></a>Comentarios

La **función FBadPropTag** valida la etiqueta de propiedad especificada en función de las definiciones MAPI. Se asegura de que el tipo de propiedad es uno de los tipos definidos por MAPI y que el identificador de propiedad está definido para ser de ese tipo. 
  
## <a name="see-also"></a>Consulte también



[FBadProp](fbadprop.md)

