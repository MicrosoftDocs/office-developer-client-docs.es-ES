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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419642"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca una propiedad especificada en un conjunto de propiedades.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> [in] Etiqueta de la propiedad que se buscará en el conjunto de propiedades, indicado por el _parámetro lpPropArray._ 
    
 _cValues_
  
> [in] Recuento de propiedades en el conjunto de propiedades, indicado por el _parámetro lpPropArray._ 
    
 _lpPropArray_
  
> [in] Matriz de **estructuras SPropValue** que define las propiedades que se buscarán. 
    
## <a name="return-value"></a>Valor devuelto

La **función LpValFindProp** devuelve una estructura **SPropValue** que define la propiedad que coincide con la etiqueta de propiedad de entrada o NULL si no hay ninguna coincidencia. 
  
## <a name="remarks"></a>Comentarios

La **función LpValFindProp** es idéntica a **PpropFindProp**.
  
## <a name="see-also"></a>Vea también



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

