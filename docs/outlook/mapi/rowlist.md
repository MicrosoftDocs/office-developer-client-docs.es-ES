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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820541"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Se aplica a**: Outlook 
  
Contiene una matriz de estructuras [ROWENTRY](rowentry.md) que representa las filas y las operaciones que se realizan en las filas de una tabla a través de la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Miembros

 **cEntries**
  
> Número de entradas en la matriz especificada por el miembro **aEntries** . 
    
 **aEntries [MAPI_DIM]**
  
> Matriz de estructuras **ROWENTRY** que contiene las filas y las operaciones que se realizan en las filas de la tabla. 
    
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Se usa para crear una lista de reglas seleccionadas para **ModifyTable** las acciones posteriores.  <br/> |
   
## <a name="see-also"></a>Ver también



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)


[Estructuras MAPI](mapi-structures.md)

