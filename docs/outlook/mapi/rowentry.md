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
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436037"
---
# <a name="rowentry"></a>ROWENTRY

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una fila y la operación que se realiza en esa fila en una tabla a través de la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>Members

**ulRowFlags**
  
> Una de las siguientes operaciones que se realizarán en los datos: 
    
  - ROW_ADD: Agregue los datos a la tabla como una fila nueva.
      
  - ROW_MODIFY: modifique esta fila en la tabla.
      
  - ROW_REMOVE: quitar esta fila de la tabla.
      
  - ROW_EMPTY: no agregue los datos de fila a la tabla. (La fila está vacía).
    
**cValues**
  
> Número de valores de propiedad en **rgPropvals**.
    
**rgPropVals**
  
> Matriz de estructuras [SPropValue](spropvalue.md) que representa los valores de las columnas que se van a insertar en la tabla. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: GetSelectedItems  <br/> |Se usa para crear una lista de reglas seleccionadas para las siguientes acciones **ModifyTable** .  <br/> |
   
## <a name="see-also"></a>Ver también
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Estructuras MAPI](mapi-structures.md)

