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
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418375"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera una fila en función de su posición en la tabla. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Parameters

 _ulRowNumber_
  
> [in] Número de fila para la que se devuelven las propiedades. El valor del parámetro  _ulRowNumber_ puede ser cualquier valor desde 0, que indica la primera fila de la tabla, a través de n - 1, que indica la última fila de la tabla. 
    
 _lppSRow_
  
> [salida] Puntero a un puntero a una [estructura SRow](srow.md) que describe la fila de destino. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se recuperó correctamente o no existe una fila para el número de fila especificado por el _parámetro ulRowNumber._ 
    
## <a name="remarks"></a>Comentarios

El **método ITableData::HrEnumRow** recupera una fila basada en un número secuencial. Este número representa el orden de inserción (0 indica la primera fila y el número de filas menos 1 indica la última fila). MAPI mantiene este orden cronológico de inserción de filas durante la duración del objeto de datos de tabla. 
  
Si el número especificado en  _ulRowNumber_ no corresponde a una fila de la tabla, **HrEnumRow** devuelve S_OK y establece el parámetro  _lppSRow_ en NULL. 
  
MAPI asigna memoria para la estructura **SRow** devuelta mediante la [función MAPIAllocateBuffer](mapiallocatebuffer.md) cuando se crea el objeto de datos de tabla. El autor de la llamada debe liberar esta memoria llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para recuperar filas de una tabla en el orden en que se insertaron, los usuarios del objeto de datos de tabla llaman al **método HrEnumRow.** 
  
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

