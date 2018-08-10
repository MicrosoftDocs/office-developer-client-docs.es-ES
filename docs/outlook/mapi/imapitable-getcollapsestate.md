---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2c1246c46e9723cd3f6d92f0a44fc1419eef4a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817583"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Hace referencia a**: Outlook 
  
Devuelve los datos que es necesario volver a generar la actual contraído o expandido el estado de una tabla con categorías.
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> Reservado; debe ser cero.
    
 _cbInstanceKey_
  
> [entrada] El número de bytes de la clave de la instancia indicada por el parámetro _lpbInstanceKey_ . 
    
 _lpbInstanceKey_
  
> [entrada] Debe recompilar un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la fila en la que la actual, contrae o expande el estado. El parámetro _lpbInstanceKey_ no puede ser NULL. 
    
 _lpcbCollapseState_
  
> [out] Un puntero para el recuento de estructuras indicada por el parámetro _lppbCollapseState_ . 
    
 _lppbCollapseState_
  
> [out] Un puntero a un puntero a estructuras que contienen datos que se describen la vista de tabla actual.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de la tabla con categorías se guardó correctamente.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la operación de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no admite la categorización y vistas expandida y contraída.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::GetCollapseState** funciona con el método [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) para cambiar la vista del usuario de una tabla con categorías. **GetCollapseState** guarda los datos que se necesitan para que **SetCollapseState** a usar para volver a generar las vistas de las categorías de una tabla con categorías adecuadas. Proveedores de servicios de determinan los datos que se guarde. Sin embargo, la mayoría de los proveedores de servicio implementar **GetCollapseState** guarda lo siguiente: 
  
- Las claves de ordenación (estándares columnas y columnas de categoría).
    
- Información acerca de la fila que representa la clave de instancia.
    
- Información para restaurar las categorías contraídas y expandidas de la tabla.
    
Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Almacenar el estado actual de todos los nodos de una tabla en el parámetro _lppbCollapseState_ . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame siempre a **GetCollapseState** antes de llamar a **SetCollapseState**. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

