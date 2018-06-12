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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 92540159386e6f37d93684aff037b235071010f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817985"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Se aplica a**: Outlook 
  
Recupera una fila de tabla.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Sintaxis

 _lpSPropValue_
  
> [entrada] Un puntero a una estructura de valor de propiedad que describe la columna de índice de la fila que se va a recuperar. El miembro **ulPropTag** de la estructura del valor de propiedad debe contener la misma etiqueta de propiedad como el parámetro _ulPropTagIndexColumn_ de la llamada a la función [CreateTable](createtable.md) , que obtiene acceso a la implementación de [ITableData](itabledataiunknown.md) . 
    
 _lppSRow_
  
> [out] Un puntero a un puntero a la fila recuperada. 
    
 _lpuliRow_
  
> [entrada, salida] En la entrada, un puntero válido o NULL, que indica que no hay información necesita que se devolverá. En la salida, un puntero válido que apunta al número de fila de la fila, un número secuencial que identifica la posición de la fila en la tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se recuperó correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
> El [SPropValue](spropvalue.md) estructura que señala _lpSPropValue_ no contiene la propiedad de columna de índice. 
    
## <a name="remarks"></a>Notas

El método **ITableData::HrQueryRow** recupera todas las propiedades de la fila que tiene una columna de índice que coincide con el valor de la columna de índice incluido en la estructura de propiedad que señala _lpSPropValue_. **HrQueryRow** también devuelve el número de fila, si el autor de la llamada lo solicita, que identifica la posición de la fila en la tabla. 
  
Debido a que **HrQueryRow** no modifique la estructura de **SPropValue** que señala _lpSPropValue_, los autores de llamadas deben liberar la estructura cuando devuelve **HrQueryRow** . Los autores de llamadas también deben liberar la estructura **SRow** que contiene la fila recuperada. 
  
## <a name="see-also"></a>Ver también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

