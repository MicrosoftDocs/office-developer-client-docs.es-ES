---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 51c239897e5e225a0765f78404526e2836371f30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567905"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Vuelve a crear el estado actual de expandidos o contraído de una tabla con categorías utilizando los datos que se guardan por una llamada anterior al método [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) . 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> Reservado; debe ser cero.
    
 _cbCollapseState_
  
> [entrada] Recuento de bytes de la estructura que señala el parámetro _pbCollapseState_ . 
    
 _pbCollapseState_
  
> [entrada] Puntero a las estructuras que contiene los datos necesarios para volver a generar la vista de tabla.
    
 _lpbkLocation_
  
> [out] Puntero a un marcador que identifica la fila de la tabla a la que debe recompilar el estado contraído o expandido. Este marcador y la clave de instancia que se pasa en el parámetro _lpbInstanceKey_ en la llamada a [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identifican la misma fila. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de la tabla con categorías volvió a generar correctamente.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la operación de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> La tabla no puede terminar de volver a generar la vista contraída o expandida.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::SetCollapseState** restablece el estado expandido o contraído de la vista de tabla. **SetCollapseState** y **GetCollapseState** trabajan juntos como sigue: 
  
1. Cuando el estado de una tabla con categorías se va a cambiar, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) se llama para guardar todos los datos relacionados con el estado antes de realizar el cambio. 
    
2. Para restaurar la vista de la tabla a su estado guardado, se denomina **SetCollapseState** . Los datos guardados por **GetCollapseState** se pasan al **SetCollapseState**. **SetCollapseState** es capaz de utilizar esos datos para restaurar el estado. 
    
3. **SetCollapseState** devuelve como un parámetro de salida de un marcador que identifica la misma fila que la clave de la instancia que se pasa como entrada en **GetCollapseState**.
    
Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Usted es responsable de comprobar que el criterio de ordenación y restricciones son exactamente los mismos tal como se administraban en el momento de la llamada **GetCollapseState** . Si se ha realizado un cambio, no debe llamarse **SetCollapseState** debido a que los resultados pueden ser impredecibles. Esto puede ocurrir si, por ejemplo, un cliente llama a **GetCollapseState** y, a continuación, **SortTable** para cambiar el criterio de ordenación antes de llamar a **SetCollapseState**. Para estar seguro, compruebe que los datos guardados todavía están válidos antes de continuar con la restauración. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para llamar a **SetCollapseState**, debe haber llamado anteriormente **GetCollapseState**. El establecimiento de las categorías de criterio de ordenación debe ser el mismo para ambos métodos. Si difieren de los criterios de ordenación, los resultados de la operación de **SetCollapseState** son imprevisibles. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

