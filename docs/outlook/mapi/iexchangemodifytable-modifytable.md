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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817184"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Se aplica a**: Outlook 
  
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
   
## <a name="see-also"></a>Ver también



[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

