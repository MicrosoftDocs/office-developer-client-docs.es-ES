---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578580"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida un criterio de ordenación establecer comprobando su asignación de memoria. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Parámetros

 _lpsos_
  
> [entrada] Puntero a una estructura [SSortOrderSet](ssortorderset.md) que identifica el criterio de ordenación establecer que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> El conjunto de criterio de ordenación especificado no es válido. 
    
FALSE 
  
> El conjunto de criterio de ordenación especificado es válido.
    
## <a name="remarks"></a>Comentarios

La función **FBadSortOrderSet** se puede usar para preparar una llamada a un método de ordenación como el método [SortTable](imapitable-sorttable.md) . 
  

