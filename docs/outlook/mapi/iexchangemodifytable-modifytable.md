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
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418179"
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

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Use uno de los siguientes valores: 
    
0 (cero)
  
> Use el valor del miembro **ulRowFlags** de la [estructura ROWENTRY.](rowentry.md) 
    
ACLTABLE_FREEBUSY
  
> Establece nuevos derechos.
    
frightsFreeBusyDetailed
  
> Cuando ACLTABLE_FREEBUSY se pasa, proporciona una visualización detallada de los nuevos derechos de disponibilidad.
    
frightsFreeBusySimple
  
> Cuando ACLTABLE_FREEBUSY se pasa, proporciona una presentación sencilla de los nuevos derechos de disponibilidad.
    
ROWLIST_REPLACE
  
> Reemplace todas las filas de la tabla.
    
 _lpMods_
  
> [entrada] Apunta a una [estructura ROWLIST](rowlist.md) que contiene las propiedades del objeto de tabla. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI usa el **método IExchangeModifyTable::ModifyTable** para volver a escribir una regla modificada en la tabla de reglas.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

