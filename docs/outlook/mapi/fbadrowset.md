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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411795"
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
  
> [entrada] Puntero a una [estructura SRowSet](srowset.md) que identifica el conjunto de filas que se va a validar. Si el puntero es NULL, la estructura no es válida. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Una fila del conjunto de filas especificado no es válida o el propio conjunto de filas no es válido. 
    
FALSE 
  
> Todas las filas del conjunto de filas especificado y el propio conjunto de filas son válidas.
    
## <a name="see-also"></a>Consulte también



[FBadRow](fbadrow.md)

