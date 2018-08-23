---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d28ce67c6b45f3d0b04d645946ea3f4b3a263c48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578993"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a una interfaz para un objeto de tabla MAPI.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser 0 (cero).
    
ACLTABLE_FREEBUSY
  
> Establece los derechos de nuevo.
    
frightsFreeBusyDetailed
  
> Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación detallada de derechos de libre/ocupado de nuevo.
    
frightsFreeBusySimple
  
> Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación sencilla libre/ocupado de derechos de nueva.
    
 _lppTable_
  
> [out] Apunta a un [IMAPITable: IUnknown](imapitableiunknown.md) interfaz que contiene el objeto table. 
    
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI usa el método **IExchangeModifyTable::GetTable** para obtener una tabla de reglas.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

