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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4117558d27d64444cdac62651584fe6cfe8ff061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583970"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

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
    
## <a name="remarks"></a>Comentarios

El parámetro _pcb_ a la función **ScRelocNotifications** es opcional. 
  
## <a name="see-also"></a>Recursos adicionales



[ScRelocProps](screlocprops.md)

