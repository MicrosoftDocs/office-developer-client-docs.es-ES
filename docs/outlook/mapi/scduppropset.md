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
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406020"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Duplica una matriz de valores de propiedad en un único bloque de memoria MAPI que combina las operaciones de las funciones [ScCopyProps](sccopyprops.md) y [ScCountProps.](sccountprops.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> [in] Recuento de valores de propiedad en la matriz indicada por el _parámetro rgprop._ 
    
 _rgprop_
  
> [in] Puntero a una matriz de [estructuras SPropValue](spropvalue.md) que definen los valores de propiedad que se deben duplicar. 
    
 _lpAllocateBuffer_
  
> [in] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria a la matriz duplicada. 
    
 _prgprop_
  
> [salida] Puntero a la posición inicial en la memoria donde se almacena la matriz duplicada devuelta de estructuras **SPropValue.** 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    

