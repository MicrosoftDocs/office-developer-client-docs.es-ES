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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436079"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve los datos necesarios para volver a generar el estado contraído o expandido actual de una tabla categorizada.
  
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
  
> Reservado; debe ser cero.
    
 _cbInstanceKey_
  
> [in] Recuento de bytes en la clave de instancia a la que apunta el _parámetro lpbInstanceKey._ 
    
 _lpbInstanceKey_
  
> [in] Puntero a la **propiedad PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la fila en la que se debe volver a generar el estado contraído o expandido actual. El  _parámetro lpbInstanceKey_ no puede ser NULL. 
    
 _lpcbCollapseState_
  
> [salida] Puntero al recuento de estructuras apuntadas por el _parámetro lppbCollapseState._ 
    
 _lppbCollapseState_
  
> [salida] Puntero a un puntero a estructuras que contienen datos que describen la vista de tabla actual.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de la tabla categorizada se guardó correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación. Debe permitirse completar la operación en curso o detenerse.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no admite categorización y vistas expandida y contraida.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::GetCollapseState** funciona con el método [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) para cambiar la vista del usuario de una tabla categorizada. **GetCollapseState** guarda los datos necesarios para que **SetCollapseState** lo use para volver a generar las vistas adecuadas de las categorías de una tabla categorizada. Los proveedores de servicios determinan los datos que se guardarán. Sin embargo, la mayoría de los proveedores de servicios que **implementan GetCollapseState** guarda lo siguiente: 
  
- Las claves de ordenación (columnas estándar y columnas de categoría).
    
- Información sobre la fila que representa la clave de instancia.
    
- Información para restaurar las categorías contraídos y expandido de la tabla.
    
Para obtener más información acerca de las tablas categorizadas, vea [Sorting and Categorization](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Almacene el estado actual de todos los nodos de una tabla en el _parámetro lppbCollapseState._ 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame siempre **a GetCollapseState antes** de llamar a **SetCollapseState**. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

