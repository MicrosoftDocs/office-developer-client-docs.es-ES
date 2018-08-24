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
ms.openlocfilehash: 0eb0374788da629c4c28eff2fce93536cf65a4ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582990"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Crea una vista de tabla, la devolución de un puntero a una implementación [IMAPITable](imapitableiunknown.md) . 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>Parámetros

 _lpSSortOrderSet_
  
> [entrada] Un puntero a una estructura de criterio de ordenación que describe el criterio de ordenación para la vista de tabla. Si se pasa NULL en el parámetro _lpSSortOrderSet_ , no se ordena la vista. 
    
 _lpfCallerRelease_
  
> [entrada] Un puntero a una función de devolución de llamada según el prototipo [CALLERRELEASE](callerrelease.md) que llama MAPI cuando suelta la vista. Si se pasa NULL en el parámetro _lpfCallerRelease_ , ninguna función se llama en la versión de la vista. 
    
 _ulCallerData_
  
> [entrada] Los datos que se deben guardar con la nueva vista y se pasan a la función de devolución de llamada que señala _lpfCallerRelease_.
    
 _lppMAPITable_
  
> [out] Un puntero a un puntero a la vista recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La vista se ha creado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **ITableData::HrGetView** crea una vista de solo lectura de los datos en la tabla, se ordenan en el orden que apunta el parámetro _lpSSortOrderSet_ . Se coloca el cursor al principio de la primera fila en la vista. Se devuelve una implementación de interfaz **IMAPITable** para obtener acceso a la vista. 
  
Proveedores de servicios de llamada **HrGetView** cuando sea necesario proporcionar un acceso de cliente a una tabla. **HrGetView** crea la vista y devuelve el puntero **IMAPITable** . Proveedores de servicios a su vez pasan el puntero de la sesión en el cliente. Cuando el cliente haya terminado de usar la tabla y llama a su método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** llama a la función de devolución de llamada indicada por el parámetro _lpfCallerRelease_ . 
  
Si necesita un proveedor de servicios para volver a un cliente de una vista que tenga una columna personalizada o una restricción, el proveedor puede llamar a los métodos la vista [IMAPITable::SetColumns](imapitable-setcolumns.md) e [IMAPITable:: Restrict](imapitable-restrict.md) antes de permitir el acceso de cliente. 
  
## <a name="see-also"></a>Vea también



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

