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
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408729"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada que puede liberar un objeto de datos de tabla cuando se libera una vista de tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Función definida implementada por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
|Función definida llamada por:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Parámetros

 _ulCallerData_
  
> [entrada] Datos del autor de la llamada guardados por MAPI con la vista de tabla y pasados a la función de devolución de llamada basada en **CALLERRELEASE.** Los datos proporcionan contexto sobre la vista de tabla que se está liberando. 
    
 _lpTblData_
  
> [entrada] Puntero a la [interfaz ITableData : IUnknown](itabledataiunknown.md) para el objeto de datos de tabla subyacente a la vista de tabla que se va a liberar. 
    
 _lpVue_
  
> [entrada] Puntero a la [interfaz IMAPITable : IUnknown](imapitableiunknown.md) para la vista de tabla que se está liberando. Se trata de una interfaz para el objeto de tabla devuelto en el parámetro  _lppMAPITable_ del método [ITableData::HrGetView](itabledata-hrgetview.md) que creó el objeto para liberar. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno 
  
## <a name="remarks"></a>Comentarios

Una aplicación cliente o un proveedor de servicios que haya rellenado un objeto de datos de tabla puede llamar a [ITableData::HrGetView](itabledata-hrgetview.md) para crear una vista ordenada de solo lectura de la tabla. La llamada a **HrGetView** pasa un puntero a una función de devolución de llamada basada en **CALLERRELEASE** y también un contexto que se guardará con la vista de tabla. Cuando el recuento de referencias de la vista de tabla vuelve a cero y se libera la vista, la implementación de **IMAPITable** llama a la función de devolución de llamada y pasa el contexto en el parámetro _ulCallerData._ 
  
Un uso común de una función de devolución de llamada basada en **CALLERRELEASE** es liberar el objeto de datos de tabla subyacente y no es necesario realizar un seguimiento de él durante el procesamiento posterior. 
  

