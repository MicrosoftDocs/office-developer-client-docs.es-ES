---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420622"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una fila de una tabla.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Parámetros

 _lprow_
  
> [in] Puntero a una [estructura SRow](srow.md) que identifica la fila que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La fila especificada no es válida.
    
FALSE 
  
> La fila especificada es válida.
    
## <a name="see-also"></a>Vea también



[FBadRowSet](fbadrowset.md)

