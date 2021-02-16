---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407553"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera el criterio de ordenación actual de una tabla.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Parámetros

 _lppSortCriteria_
  
> [salida] Puntero a un puntero a la [estructura SSortOrderSet](ssortorderset.md) que mantiene el criterio de ordenación actual. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El criterio de ordenación actual se devolvió correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de recuperación de criterio de ordenación. La operación en curso debe poder completarse o debe detenerse.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::QuerySortOrder** recupera el criterio de ordenación actual de una tabla. Los pedidos de ordenación se describen con una [estructura SSortOrderSet.](ssortorderset.md) 
  
- El **miembro cSorts** de la estructura **SSortOrderSet** se puede establecer en cero si: 
    
- La tabla no está desordenada.
    
- No hay información sobre cómo se ordena la tabla.
    
- La **estructura SSortOrderSet** no es adecuada para describir el criterio de ordenación. 
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si se realiza una llamada al método [IMAPITable::SortTable](imapitable-sorttable.md) con una estructura **SSortOrderSet** que contiene cero columnas en la clave de ordenación, quite el criterio de ordenación actual y aplique el orden predeterminado, si lo hay. En llamadas posteriores **a QuerySortOrder,** puede elegir si desea devolver cero o más columnas para la clave de ordenación. Puede devolver más columnas de las que se encuentran en la vista actual.
  
Para obtener más información acerca de la ordenación, vea [Ordenar y categorizar](sorting-and-categorization.md).
  
## <a name="see-also"></a>Consulte también



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

