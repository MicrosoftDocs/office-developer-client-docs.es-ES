---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434770"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera una fila de tabla.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Parámetros

 _lpSPropValue_
  
> [entrada] Puntero a una estructura de valores de propiedad que describe la columna de índice de la fila que se va a recuperar. El **miembro ulPropTag** de la estructura de valores de propiedad debe contener la misma etiqueta de propiedad que el parámetro _ulPropTagIndexColumn_ de la llamada a la función [CreateTable,](createtable.md) que tiene acceso a la implementación [de ITableData.](itabledataiunknown.md) 
    
 _lppSRow_
  
> [salida] Puntero a un puntero a la fila recuperada. 
    
 _lpuliRow_
  
> [entrada, salida] En la entrada, un puntero válido o NULL, que indica que no es necesario devolver información. En el resultado, un puntero válido que apunta al número de fila de la fila, un número secuencial que identifica la posición de la fila en la tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se recuperó correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
> La [estructura SPropValue](spropvalue.md) a la que  _apunta lpSPropValue_ no contiene la propiedad de columna de índice. 
    
## <a name="remarks"></a>Comentarios

El **método ITableData::HrQueryRow** recupera todas las propiedades de la fila que tiene una columna de índice que coincide con el valor de la columna de índice incluida en la estructura de propiedades a la que apunta  _lpSPropValue_. **HrQueryRow** también devuelve el número de fila, si el autor de la llamada lo solicita, que identifica la posición de la fila en la tabla. 
  
Debido **a que HrQueryRow** no modifica la estructura **SPropValue** a la que apunta  _lpSPropValue_, los autores de llamadas deben liberar la estructura cuando **HrQueryRow** devuelve. Los autores de llamadas también deben liberar la **estructura SRow** que contiene la fila recuperada. 
  
## <a name="see-also"></a>Consulte también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

