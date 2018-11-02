---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fb0bfaba1ca0a0d7d34096b3b0b1db9863207097
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576270"
---
# <a name="rowentry"></a>ROWENTRY

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una fila y la operación que se lleva a cabo en esa fila en una tabla a través de la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>Miembros

**ulRowFlags**
  
> Una de las siguientes operaciones se realicen en los datos: 
    
  - ROW_ADD: Agregar los datos a la tabla como una nueva fila.
      
  - ROW_MODIFY: Modificar esta fila en la tabla.
      
  - ROW_REMOVE: Quitar esta fila de la tabla.
      
  - ROW_EMPTY: No agregue la fila de datos a la tabla. (La fila está vacía).
    
**cValues**
  
> El número de valores de propiedad en **rgPropvals**.
    
**rgPropVals**
  
> Una matriz de estructuras [SPropValue](spropvalue.md) que representa los valores de las columnas que se insertará en la tabla. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Se usa para crear una lista de reglas seleccionadas para **ModifyTable** las acciones posteriores.  <br/> |
   
## <a name="see-also"></a>Vea también
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Estructuras MAPI](mapi-structures.md)

