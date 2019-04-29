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
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414070"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Vuelve a compilar el estado expandido o contraído actual de una tabla clasificada con datos que se guardaron mediante una llamada anterior al método [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) . 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Reserve debe ser cero.
    
 _cbCollapseState_
  
> a Número de bytes en la estructura a la que apunta el parámetro _pbCollapseState_ . 
    
 _pbCollapseState_
  
> a Puntero a las estructuras que contienen los datos necesarios para volver a crear la vista de tabla.
    
 _lpbkLocation_
  
> contempla Puntero a un marcador que identifica la fila de la tabla en la que se debe recompilar el estado contraído o expandido. Este marcador y la clave de instancia pasada en el parámetro _lpbInstanceKey_ en la llamada a [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) identifican la misma fila. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de la tabla clasificada se reconstruyó correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que la operación se inicie. Debe permitirse que la operación en curso se complete o que deba detenerse.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> La tabla no pudo terminar de volver a crear la vista contraída o expandida.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: SetCollapseState** restablece el estado expandido o contraído de la vista de tabla. **SetCollapseState** y **GetCollapseState** trabajan juntos de la siguiente manera: 
  
1. Cuando se va a cambiar el estado de una tabla clasificada, se llama a [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) para guardar todos los datos pertenecientes al estado antes del cambio. 
    
2. Para restaurar la vista de la tabla a su estado guardado, se llama a **SetCollapseState** . Los datos guardados por **GetCollapseState** se pasan a **SetCollapseState**. **SetCollapseState** puede usar esos datos para restaurar el estado. 
    
3. **SetCollapseState** devuelve como parámetro de salida un marcador que identifica la misma fila que la clave de instancia pasada como entrada a **GetCollapseState**.
    
Para obtener más información acerca de las tablas clasificadas por categorías, vea [ordenar y categorización](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Usted es responsable de comprobar que el criterio de ordenación y las restricciones son exactamente iguales a los que estaban en el momento de la llamada **GetCollapseState** . Si se ha realizado un cambio, no se debe llamar a **SetCollapseState** porque los resultados pueden ser imprevisibles. Esto puede ocurrir si, por ejemplo, un cliente llama a **GetCollapseState** y, a continuación, **SortTable** cambiar la clave de ordenación antes de llamar a **SetCollapseState**. Para ser seguro, compruebe que los datos guardados siguen siendo válidos antes de continuar con la restauración. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para llamar a **SetCollapseState**, debe haber llamado previamente a **GetCollapseState**. El criterio de ordenación que establece las categorías debe ser el mismo para ambos métodos. Si los criterios de ordenación son distintos, los resultados de la operación **SetCollapseState** son imprevisibles. 
  
## <a name="see-also"></a>Ver también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

