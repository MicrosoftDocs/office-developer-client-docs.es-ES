---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816781"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Hace referencia a**: Outlook 
  
Valida una propiedad especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Parámetros

 _lpProp_
  
> [entrada] Una estructura [SPropValue](spropvalue.md) definición de la propiedad que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La propiedad especificada no es válida. 
    
FALSE 
  
> La propiedad especificada es válida.
    
## <a name="remarks"></a>Comentarios

Un proveedor de servicios puede llamar a la función **FBadProp** por varias razones, por ejemplo, para preparar una llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) al establecer una propiedad. **FBadProp** valida la propiedad especificada según el tipo de propiedad. Por ejemplo, si la propiedad es Boolean, **FBadProp** hacer sures que su valor es TRUE o FALSE. Si la propiedad es binario, **FBadProp** comprueba su puntero y su tamaño y se asegura de que está asignado correctamente. 
  
## <a name="see-also"></a>Vea también



[FBadPropTag](fbadproptag.md)

