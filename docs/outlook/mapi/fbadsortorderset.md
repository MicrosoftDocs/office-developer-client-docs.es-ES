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
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428462"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida un criterio de ordenación establecido mediante la comprobación de la asignación de memoria. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Parámetros

 _lpsos_
  
> a Puntero a una estructura [SSortOrderSet](ssortorderset.md) que identifica el criterio de ordenación establecido para validarse. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> El conjunto de criterios de ordenación especificado no es válido. 
    
FALSE 
  
> El conjunto de criterio de ordenación especificado es válido.
    
## <a name="remarks"></a>Comentarios

La función **FBadSortOrderSet** se puede usar para preparar una llamada a un método de ordenación como el método [IMAPITable:: SortTable](imapitable-sorttable.md) . 
  

