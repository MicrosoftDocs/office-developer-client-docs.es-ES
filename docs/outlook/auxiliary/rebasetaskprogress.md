---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Informes de progreso para enumeración y reajuste de citas.
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816339"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Informes de progreso para enumeración y reajuste de citas.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |tzmovelib.h  <br/> |
|Se implementa mediante:  <br/> |Aplicaciones cliente MAPI  <br/> |
|Llamado por:  <br/> |Objeto de reajuste de Outlook  <br/> |
|Tipo de puntero:  <br/> |**PFNREBASETASKPROGRESS** tal como se define en tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>Sintaxis

_ulMin_
  
> [entrada] El extremo inferior del intervalo de citas que se está procesando. Normalmente, es cero.
    
_ulMax_
  
> [entrada] Alta final del intervalo de citas que se está procesando. Suele ser el número de elementos en la carpeta de calendario que se está procesando.
    
_ulCur_
  
> [entrada] El elemento actual que se está procesando.
    
_State_
  
> [entrada] Un valor que indica el estado de la que se está procesando. La enumeración **REBASE_APPT_STATE** se define en tzmovelib.h.  _Estado_ es uno de los siguientes valores: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** : examen y examen de un elemento. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** : examen y que se encuentre un elemento. 
    
   - **REBASE_APPT_STATE_BEGIN** : fijación e inicio de un elemento. 
    
   - **REBASE_APPT_STATE_REBASING** : fijación y el ajuste de un elemento. 
    
   - **REBASE_APPT_STATE_SENDING** : fijación y enviar una actualización de la reunión. 
    
   - **REBASE_APPT_STATE_DONE** : fijación y listo con un elemento. 
    
_pRowCur_
  
> [entrada] Un puntero a una estructura **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que describe el elemento que se examinan o fijo. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Las aplicaciones de cliente MAPI que usan la interfaz [IOlkApptRebaser](iolkapptrebaser.md) implementan esta función para realizar un seguimiento de procesamiento del elemento. 
  
## <a name="see-also"></a>Ver también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

