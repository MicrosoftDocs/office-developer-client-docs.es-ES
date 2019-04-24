---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Informa del progreso de la enumeración y el reajuste de las citas.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326456"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Informa del progreso de la enumeración y el reajuste de las citas.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |tzmovelib. h  <br/> |
|Implementado por:  <br/> |Aplicaciones cliente de MAPI  <br/> |
|Llamado por:  <br/> |Objeto de reajuste de Outlook  <br/> |
|Tipo de puntero:  <br/> |**PFNREBASETASKPROGRESS** como se define en tzmovelib. h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>Parameters

_ulMin_
  
> a El extremo inferior del intervalo de citas que se está procesando. Suele ser cero.
    
_ulMax_
  
> a El extremo superior del intervalo de citas que se está procesando. Suele ser el número de elementos de la carpeta de calendario que se está procesando.
    
_ulCur_
  
> a Elemento actual que se está procesando.
    
_State_
  
> a Un valor que indica el estado del elemento que se está procesando. La enumeración **REBASE_APPT_STATE** se define en tzmovelib. h.  _State_ es uno de los siguientes valores: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** : análisis y examen de un elemento. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** : análisis y encontrado un elemento. 
    
   - **REBASE_APPT_STATE_BEGIN** : corrección e inicio de un elemento. 
    
   - **REBASE_APPT_STATE_REBASING** : corrección y ajuste de un elemento. 
    
   - **REBASE_APPT_STATE_SENDING** : corrección y envío de una actualización de la reunión. 
    
   - **REBASE_APPT_STATE_DONE** : se corrige y se hace con un elemento. 
    
_pRowCur_
  
> a Un puntero a una estructura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que describe el elemento que se está examinando o corrigiendo. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Las aplicaciones de cliente MAPI que usan la interfaz [IOlkApptRebaser](iolkapptrebaser.md) implementan esta función para realizar un seguimiento del procesamiento de elementos. 
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

