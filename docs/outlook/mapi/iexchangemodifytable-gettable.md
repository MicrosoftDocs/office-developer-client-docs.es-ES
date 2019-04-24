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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336620"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a una interfaz para un objeto Table de MAPI.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Reserve debe ser 0 (cero).
    
ACLTABLE_FREEBUSY
  
> Establece nuevos derechos.
    
frightsFreeBusyDetailed
  
> Cuando se pasa ACLTABLE_FREEBUSY, proporciona una visualización detallada de los nuevos derechos de disponibilidad.
    
frightsFreeBusySimple
  
> Cuando se pasa ACLTABLE_FREEBUSY, proporciona una visualización sencilla de los nuevos derechos de disponibilidad.
    
 _lppTable_
  
> contempla Apunta a una interfaz [IMAPITable: IUnknown](imapitableiunknown.md) que contiene el objeto de tabla. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: OnRefreshView  <br/> |MFCMAPI usa el método **IExchangeModifyTable:: GetTable** para obtener una tabla de reglas.  <br/> |
   
## <a name="see-also"></a>Vea también



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

