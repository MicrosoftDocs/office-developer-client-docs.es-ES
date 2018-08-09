---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b93f84026cacd8568dc5ceec5574d144f6d1633
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820590"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Hace referencia a**: Outlook 
  
Duplica una matriz de valores de propiedad en un único bloque de memoria MAPI combinar las operaciones de las funciones [ScCopyProps](sccopyprops.md) y [ScCountProps](sccountprops.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>Parámetros

 _cprop_
  
> [entrada] Recuento de valores de propiedad en la matriz indicada por el parámetro _rgprop_ . 
    
 _rgprop_
  
> [entrada] Puntero a una matriz de estructuras [SPropValue](spropvalue.md) definición de los valores de propiedad que se va a duplicar. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria para la matriz duplicada. 
    
 _prgprop_
  
> [out] Puntero a la posición inicial en la memoria donde se almacena la matriz devuelta duplicada de estructuras **SPropValue** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    

