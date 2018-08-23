---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b801bdc06317738448a2205b60b94e1c9707d4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565910"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Actualiza un objeto de tabla MAPI.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Use uno de los siguientes valores: 
    
0 (cero)
  
> Use el valor del miembro **ulRowFlags** de la estructura [ROWENTRY](rowentry.md) . 
    
ACLTABLE_FREEBUSY
  
> Establece los derechos de nuevo.
    
frightsFreeBusyDetailed
  
> Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación detallada de derechos de libre/ocupado de nuevo.
    
frightsFreeBusySimple
  
> Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación sencilla libre/ocupado de derechos de nueva.
    
ROWLIST_REPLACE
  
> Reemplace todas las filas de la tabla.
    
 _lpMods_
  
> [entrada] Apunta a una estructura [ROWLIST](rowlist.md) que contiene las propiedades para el objeto table. 
    
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI usa el método **IExchangeModifyTable::ModifyTable** volver a escribir una regla modificada en la tabla de reglas.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

