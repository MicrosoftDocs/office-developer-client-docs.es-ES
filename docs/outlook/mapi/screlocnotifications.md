---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: bb4ff6a128b9fed29ff0be5325c21e5600389740
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820617"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Se aplica a**: Outlook 
  
Ajusta un puntero dentro de una matriz de notificación de evento especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Sintaxis

 _cntf_
  
> [entrada] Recuento de las estructuras de [notificación](notification.md) en la matriz indicada por el parámetro _rgntf_ . 
    
 _rgntf_
  
> [entrada] Puntero a la matriz de las estructuras de **notificación** para definir las notificaciones de eventos en el que es un puntero para ajustarse. 
    
 _pvBaseOld_
  
> [entrada] Puntero a la dirección base original de la matriz indicada por el parámetro _rgntf_ . 
    
 _pvBaseNew_
  
> [entrada] La ubicación a la que **ScRelocNotifications** escribe la nueva dirección de base de la matriz indicada por el parámetro _rgntf_ . 
    
 _placa de circuitos impresos_
  
> [out] Puntero al tamaño, en bytes, de la matriz indicada por el parámetro _pvBaseNew_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Un puntero se ajusta correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Se ha producido una notificación no válida.
    
## <a name="remarks"></a>Notas

El parámetro _pcb_ a la función **ScRelocNotifications** es opcional. 
  
## <a name="see-also"></a>Ver también



[ScRelocProps](screlocprops.md)

