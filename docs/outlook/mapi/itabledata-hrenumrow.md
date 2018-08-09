---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6c149a215a048b96408025e08df55972fa989f46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817969"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**Hace referencia a**: Outlook 
  
Recupera una fila en función de su posición en la tabla. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Parámetros

 _ulRowNumber_
  
> [entrada] El número de la fila que se va a devolver propiedades. El valor en el parámetro _ulRowNumber_ puede ser cualquier valor de 0, que indica que la primera fila en la tabla, a través de n - 1, que indica la última fila de la tabla. 
    
 _lppSRow_
  
> [out] Un puntero a un puntero a una estructura [SRow](srow.md) que describe la fila de destino. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se recuperó correctamente o no existe una fila para el número de fila especificado por el parámetro _ulRowNumber_ . 
    
## <a name="remarks"></a>Comentarios

El método **ITableData::HrEnumRow** recupera una fila basada en un número secuencial. Este número representa el orden de inserción (0 indica que la primera fila y el número de filas menos 1 indica la última fila). MAPI mantiene este orden cronológico de inserción de fila para el período de duración del objeto de datos de tabla. 
  
Si el número especificado en _ulRowNumber_ no corresponde a una fila en la tabla, **HrEnumRow** devuelve S_OK y establece el parámetro _lppSRow_ en NULL. 
  
MAPI asigna memoria para la estructura **SRow** devuelta mediante el uso de la función [MAPIAllocateBuffer](mapiallocatebuffer.md) cuando se crea el objeto de datos de tabla. El llamador debe liberar esta memoria mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para recuperar filas de una tabla en el orden en que se insertaron, los usuarios de objeto de datos de tabla llame al método de **HrEnumRow** . 
  
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

