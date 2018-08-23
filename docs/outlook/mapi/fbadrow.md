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
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590165"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una fila en una tabla.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Parámetros

 _lprow_
  
> [entrada] Puntero a una estructura [SRow](srow.md) que identifica la fila que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La fila especificada no es válida.
    
FALSE 
  
> La fila especificada es válida.
    
## <a name="see-also"></a>Recursos adicionales



[FBadRowSet](fbadrowset.md)

