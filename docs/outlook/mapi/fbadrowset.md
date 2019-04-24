---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341023"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida todas las filas de tabla incluidas en un conjunto de filas de tabla.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Parámetros

 _lpRowSet_
  
> a Puntero a una estructura [SRowSet](srowset.md) que identifica el conjunto de filas que se va a validar. Si el puntero es NULL, la estructura no es válida. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Una fila del conjunto de filas especificado no es válida o el conjunto de filas en sí no es válido. 
    
FALSE 
  
> Las filas del conjunto de filas especificado y el conjunto de filas son válidas.
    
## <a name="see-also"></a>Vea también



[FBadRow](fbadrow.md)

