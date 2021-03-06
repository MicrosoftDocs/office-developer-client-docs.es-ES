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
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436247"
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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Reservado; debe ser 0 (cero).
    
ACLTABLE_FREEBUSY
  
> Establece nuevos derechos.
    
frightsFreeBusyDetailed
  
> Cuando ACLTABLE_FREEBUSY se pasa, proporciona una presentación detallada de los nuevos derechos de disponibilidad.
    
frightsFreeBusySimple
  
> Cuando ACLTABLE_FREEBUSY se pasa, proporciona una presentación sencilla de los nuevos derechos de disponibilidad.
    
 _lppTable_
  
> [salida] Apunta a una [interfaz IMAPITable : IUnknown](imapitableiunknown.md) que contiene el objeto table. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI usa el **método IExchangeModifyTable::GetTable** para obtener una tabla de reglas.  <br/> |
   
## <a name="see-also"></a>Vea también



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

