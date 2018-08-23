---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578097"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establecer las búsquedas para una propiedad especificada en una propiedad.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones de cliente y los proveedores de servicios.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Parámetros

 _ulPropTag_
  
> [entrada] Etiqueta de la propiedad Buscar en el conjunto de propiedades, indicado por el parámetro _lpPropArray_ . 
    
 _cValues_
  
> [entrada] Recuento de propiedades en el conjunto de propiedades, indicada por el parámetro _lpPropArray_ . 
    
 _lpPropArray_
  
> [entrada] Matriz de estructuras **SPropValue** que define las propiedades que se desea buscar. 
    
## <a name="return-value"></a>Valor devuelto

La función **LpValFindProp** devuelve una estructura **SPropValue** que define la propiedad que coincide con la etiqueta de propiedad de entrada, o NULL si no hay ninguna coincidencia. 
  
## <a name="remarks"></a>Comentarios

La función **LpValFindProp** es idéntica a **PpropFindProp**.
  
## <a name="see-also"></a>Recursos adicionales



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

