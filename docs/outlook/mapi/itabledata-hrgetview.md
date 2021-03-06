---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278718"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una vista de tabla y devuelve un puntero a una [implementación imapitable.](imapitableiunknown.md) 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>Parameters

 _lpSSortOrderSet_
  
> [in] Puntero a una estructura de criterio de ordenación que describe el criterio de ordenación de la vista de tabla. Si se pasa NULL en el  _parámetro lpSSortOrderSet,_ la vista no se ordena. 
    
 _lpfCallerRelease_
  
> [in] Puntero a una función de devolución de llamada basada en el prototipo [CALLERRELEASE](callerrelease.md) al que LLAMA MAPI cuando libera la vista. Si se pasa NULL en el  _parámetro lpfCallerRelease,_ no se llama a ninguna función al liberar la vista. 
    
 _ulCallerData_
  
> [in] Los datos que se deben guardar con la nueva vista y pasar a la función de devolución de llamada a la que  _apunta lpfCallerRelease_.
    
 _lppMAPITable_
  
> [salida] Puntero a un puntero a la vista recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La vista se creó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método ITableData::HrGetView** crea una vista de solo lectura de los datos de la tabla, ordenada en el orden indicado por el parámetro _lpSSortOrderSet._ El cursor se coloca al principio de la primera fila de la vista. Se devuelve una implementación de interfaz **IMAPITable** para obtener acceso a la vista. 
  
Los proveedores de servicios **llaman a HrGetView** cuando necesitan dar a un cliente acceso a una tabla. **HrGetView crea** la vista y devuelve el **puntero IMAPITable.** A su vez, los proveedores de servicios pasan el puntero al cliente. Cuando el cliente termina de usar la tabla y llama a su método [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) **HrGetView** llama a la función de devolución de llamada señalada por el parámetro _lpfCallerRelease._ 
  
Si un proveedor de servicios necesita devolver a un cliente una vista que tenga un conjunto de columnas personalizado o una restricción, el proveedor puede llamar a los métodos [IMAPITable::SetColumns](imapitable-setcolumns.md) e [IMAPITable::Restrict](imapitable-restrict.md) de la vista antes de permitir el acceso del cliente. 
  
## <a name="see-also"></a>Vea también



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

