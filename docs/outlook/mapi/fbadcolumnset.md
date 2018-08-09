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
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816797"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Hace referencia a**: Outlook 
  
Las pruebas de la validez de una columna de tabla establecida para usar un proveedor de servicios en una llamada posterior al método [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Parámetros

 _lpptaCols_
  
> [entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de definición de las columnas de tabla para validar las etiquetas (propiedad). 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> El conjunto de la columna especificada no es válido. 
    
FALSE 
  
> El conjunto de columnas especificado es válido.
    
## <a name="remarks"></a>Comentarios

La función **FBadColumnSet** trata a las columnas de tipo PT_ERROR como no válida y las columnas de tipo PT_NULL como válido. 
  

