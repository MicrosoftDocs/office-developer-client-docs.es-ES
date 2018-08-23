---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e97e1d5302d8247cb09ce7cb1b581582405300a5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568135"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada que puede liberar un objeto de datos de tabla cuando se publica una vista de tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Función definido implementada por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
|Llamado por una función definida:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Parámetros

 _ulCallerData_
  
> [entrada] Datos del autor de la llamada guarda por MAPI con la vista de tabla y se pasan a la **CALLERRELEASE** en función de función de devolución de llamada. Los datos proporcionan contexto acerca de la vista de tabla que se publica. 
    
 _lpTblData_
  
> [entrada] Puntero a la [ITableData: IUnknown](itabledataiunknown.md) interfaz para el objeto de datos de tabla subyacentes de la vista de tabla que se publica. 
    
 _lpVue_
  
> [entrada] Puntero a la [IMAPITable: IUnknown](imapitableiunknown.md) interfaz para la vista de tabla que se publica. Se trata de una interfaz para el objeto table devuelto en el parámetro _lppMAPITable_ del método [ITableData::HrGetView](itabledata-hrgetview.md) que creó el objeto para liberar. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno 
  
## <a name="remarks"></a>Observaciones

Una aplicación cliente o un proveedor de servicio que se rellena un objeto de datos de tabla puede llamar a [ITableData::HrGetView](itabledata-hrgetview.md) para crear una vista de solo lectura, ordenada de la tabla. La llamada a **HrGetView** pasa un puntero a una función de devolución de llamada en función de **CALLERRELEASE** y también un contexto que se guarde con la vista de tabla. Cuando se devuelve el recuento de referencia de la vista de tabla en cero y se publica la vista, la implementación de **IMAPITable** llama a la función de devolución de llamada, pasando el contexto en el parámetro _ulCallerData_ . 
  
Un uso común de una función de devolución de llamada en función de **CALLERRELEASE** es liberar el objeto de datos de tabla subyacente y no tiene que realizar un seguimiento de durante el procesamiento subsiguiente. 
  

