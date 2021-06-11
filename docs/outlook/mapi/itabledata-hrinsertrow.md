---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435442"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inserta una fila de tabla. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameters

 _uliRow_
  
> [in] Número de fila secuencial que representa una fila específica. La nueva fila se colocará después de la fila que indica el número. El  _parámetro uliRow_ puede contiene números de fila de 0 a n, donde n es el número total de filas de la tabla. Al pasar n en  _uliRow_ se anexa la fila al final de la tabla. 
    
 _lpSRow_
  
> [in] Puntero a una [estructura SRow](srow.md) que describe la fila que se va a insertar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se insertó correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
> Una fila que tiene el mismo valor para su columna de índice que la fila que se va a insertar ya existe en la tabla.
    
## <a name="remarks"></a>Comentarios

El **método ITableData::HrInsertRow** inserta una fila en una tabla en una posición determinada. La nueva fila se inserta después de la fila que se encuentra en la posición especificada por el _parámetro uliRow._ 
  
Si  _uliRow_ se establece en el número de filas de la tabla, la nueva fila se anexa al final de la tabla. 
  
La propiedad que actúa como columna de índice para la tabla debe incluirse en el **miembro lpProps** de la [estructura SRow](srow.md) a la que apunta el _parámetro lpSRow._ Esta propiedad index, normalmente **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), se usa para identificar de forma única la fila para tareas de mantenimiento futuras.
  
Las columnas de propiedad de **la estructura SRow** no tienen que estar en el mismo orden que las columnas de propiedad de la tabla. 
  
Una vez insertada la fila, se envían notificaciones a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable::Advise](imapitable-advise.md) de la tabla para registrarse en las notificaciones. No se envía ninguna notificación si la fila insertada no se incluye en la vista debido a una restricción. 
  
## <a name="see-also"></a>Vea también



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

