---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Informa de la finalización de reajuste de citas.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388920"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Informa de la finalización de reajuste de citas.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |Aplicaciones cliente MAPI  <br/> |
|Llamado por:  <br/> |Objeto de reajuste de Outlook  <br/> |
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

## <a name="parameters"></a>Parámetros

_ulRowIndex_
  
> [entrada] La fila que se procesó. Este índice hace referencia a la estructura **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** pasada a [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_pRowCur_
  
> [entrada] un puntero a una estructura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que describe el elemento que se procesó. 
    
_hrResult_
  
> [entrada] Un **HRESULT** que indica el resultado de la operación de reajuste. 
    
_fModified_
  
> [entrada] Especifica si el elemento se ha modificado.
    
_fSentUpdate_
  
> [entrada] Especifica si el mensaje de actualización de una reunión se envió. 
    
_pError_
  
> [entrada] Un puntero a una estructura **MAPIERROR** con información de error extendida. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Las aplicaciones de cliente MAPI que usan la interfaz [IOlkApptRebaser](iolkapptrebaser.md) implementan esta función para realizar un seguimiento de la finalización de las actualizaciones del elemento. 
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

