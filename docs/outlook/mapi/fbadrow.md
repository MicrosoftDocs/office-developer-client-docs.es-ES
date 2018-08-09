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
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816814"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Hace referencia a**: Outlook 
  
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
    
## <a name="see-also"></a>Vea también



[FBadRowSet](fbadrowset.md)

