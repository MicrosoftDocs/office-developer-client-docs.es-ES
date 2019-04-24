---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346301"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de estructuras [ROWENTRY](rowentry.md) que representan las filas y las operaciones que se realizan en esas filas de una tabla a través de la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Members

 **cEntries**
  
> Número de entradas en la matriz especificada por el miembro **aEntries** . 
    
 **aEntries [MAPI_DIM]**
  
> Matriz de estructuras **ROWENTRY** que contiene las filas y las operaciones que se realizan en las filas de la tabla. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: GetSelectedItems  <br/> |Se usa para crear una lista de reglas seleccionadas para las siguientes acciones **ModifyTable** .  <br/> |
   
## <a name="see-also"></a>Vea también



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Estructuras MAPI](mapi-structures.md)

