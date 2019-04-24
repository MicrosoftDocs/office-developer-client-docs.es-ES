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
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328933"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve los datos necesarios para volver a generar el estado expandido o contraído actual de una tabla clasificada.
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Reserve debe ser cero.
    
 _cbInstanceKey_
  
> a El recuento de bytes de la clave de instancia apuntado por el parámetro _lpbInstanceKey_ . 
    
 _lpbInstanceKey_
  
> a Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la fila en la que se debe recompilar el estado expandido o contraído actual. El parámetro _lpbInstanceKey_ no puede ser nulo. 
    
 _lpcbCollapseState_
  
> contempla Un puntero al número de estructuras señalado por el parámetro _lppbCollapseState_ . 
    
 _lppbCollapseState_
  
> contempla Un puntero a un puntero a estructuras que contienen datos que describen la vista de tabla actual.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de la tabla clasificada se ha guardado correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que la operación se inicie. Debe permitirse que la operación en curso se complete o que deba detenerse.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no admite la categorización y las vistas expandidas y contraídas.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: GetCollapseState** funciona con el método [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md) para cambiar la vista del usuario de una tabla clasificada. **GetCollapseState** guarda los datos necesarios para que **SetCollapseState** use para volver a crear las vistas adecuadas de las categorías de una tabla clasificada. Los proveedores de servicios determinan los datos que se van a guardar. Sin embargo, la mayoría de los proveedores de servicios que implementan **GetCollapseState** guardan lo siguiente: 
  
- Claves de ordenación (columnas estándar y columnas de categoría).
    
- Información sobre la fila representada por la clave de instancia.
    
- Información para restaurar las categorías contraídas y expandidas de la tabla.
    
Para obtener más información acerca de las tablas clasificadas por categorías, vea [ordenar y categorización](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Almacene el estado actual de todos los nodos de una tabla en el parámetro _lppbCollapseState_ . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame siempre a **GetCollapseState** antes de llamar a **SetCollapseState**. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

