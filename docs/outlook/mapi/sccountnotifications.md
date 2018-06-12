---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c27472a309c26882051744a23fbe05e41c36aa3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820591"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Se aplica a**: Outlook 
  
Determina el tamaño, en bytes, de una matriz de las notificaciones de eventos y valida la memoria asociada a la matriz.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Sintaxis

 _cntf_
  
> [entrada] Recuento de las estructuras de [notificación](notification.md) en la matriz indicada por el parámetro _rgntf_ . 
    
 _rgntf_
  
> [entrada] Puntero a la matriz de estructuras de **notificación** cuyo tamaño es que se determinará. 
    
 _placa de circuitos impresos_
  
> [out] Puntero opcional para el tamaño, en bytes, de la matriz indicada por el parámetro _rgntf_ . Si es NULL, **ScCountNotifications** valida la matriz de notificaciones. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Recuento de determinó correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Se ha producido una notificación no válida.
    
## <a name="remarks"></a>Notas

Si se pasa NULL en el parámetro _pcb_ , la función **ScCountNotifications** sólo valida la matriz de notificaciones, pero no se realiza recuento; Si se pasa un valor no nulo en _placa de circuitos impresos_, **ScCountNotifications** determina el tamaño de la matriz y almacena la causa _placa de circuitos impresos_. El parámetro _pcb_ debe ser lo suficientemente grande como para contener toda la matriz. 
  

