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
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341044"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Valida una propiedad especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Parámetros

 _lpprop_
  
> [entrada] Una estructura [SPropValue](spropvalue.md) que define la propiedad que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La propiedad especificada no es válida. 
    
FALSE 
  
> La propiedad especificada es válida.
    
## <a name="remarks"></a>Comentarios

Un proveedor de servicios puede llamar a la función **FBadProp** por diversos motivos, por ejemplo, para prepararse para una llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) que establece una propiedad. **FBadProp** valida la propiedad especificada según el tipo de propiedad. Por ejemplo, si la propiedad es booleana, **FBadProp** se asegura de que el valor es TRUE o FALSE. Si la propiedad es binaria, **FBadProp** comprueba el puntero y el tamaño y se asegura de que se asigna correctamente. 
  
## <a name="see-also"></a>Vea también



[FBadPropTag](fbadproptag.md)

