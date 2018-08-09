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
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818035"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

