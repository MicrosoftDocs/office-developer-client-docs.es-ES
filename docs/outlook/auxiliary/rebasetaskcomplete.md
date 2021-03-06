---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Informa de la finalización para el rebasado de citas.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328325"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Informa de la finalización para el rebasado de citas.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |Aplicaciones cliente MAPI  <br/> |
|Llamado por:  <br/> |Outlook objeto de rebasado  <br/> |
|Tipo de puntero:  <br/> |**PFNREBASETASKCOMPLETE** tal como se define en tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a>Parameters

_ulRowIndex_
  
> [in] Fila que se procesó. Este índice hace referencia a la estructura **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** pasada a [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_pRowCur_
  
> in] Puntero a una **[estructura SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que describe el elemento que se procesó. 
    
_hrResult_
  
> [in] HRESULT **que** indica el resultado de la operación de rebasado. 
    
_fModified_
  
> [in] Especifica si el elemento se modificó.
    
_fSentUpdate_
  
> [in] Especifica si se envió un mensaje de actualización de reunión. 
    
_pError_
  
> [in] Puntero a una estructura **MAPIERROR** con información de error extendida. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente MAPI que usan la [interfaz IOlkApptRebaser](iolkapptrebaser.md) implementan esta función para realizar un seguimiento de la finalización de las actualizaciones de elementos. 
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

