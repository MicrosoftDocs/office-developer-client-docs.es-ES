---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434721"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprueba la validez de un conjunto de columnas de tabla para que lo use un proveedor de servicios en una llamada posterior al método [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Parámetros

 _lpptaCols_
  
> [entrada] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que definen las columnas de tabla que se validarán. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> El conjunto de columnas especificado no es válido. 
    
FALSE 
  
> El conjunto de columnas especificado es válido.
    
## <a name="remarks"></a>Comentarios

La **función FBadColumnSet** trata las columnas de tipo PT_ERROR como no válidas y las columnas de tipo PT_NULL como válidas. 
  

