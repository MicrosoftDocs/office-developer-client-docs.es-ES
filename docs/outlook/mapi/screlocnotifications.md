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
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415204"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Ajusta un puntero dentro de una matriz de notificación de eventos especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cntf_
  
> [in] Recuento de [estructuras NOTIFICATION](notification.md) en la matriz indicada por el _parámetro rgntf._ 
    
 _rgntf_
  
> [in] Puntero a la matriz de estructuras **NOTIFICATION** que definen las notificaciones de eventos en las que se va a ajustar un puntero. 
    
 _pvBaseOld_
  
> [in] Puntero a la dirección base original de la matriz indicada por el _parámetro rgntf._ 
    
 _pvBaseNew_
  
> [in] La ubicación en la **que ScRelocNotifications** escribe la nueva dirección base de la matriz indicada por el _parámetro rgntf._ 
    
 _pcb_
  
> [salida] Puntero al tamaño, en bytes, de la matriz indicada por el _parámetro pvBaseNew._ 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Un puntero se ajustó correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Se encontró una notificación no válida.
    
## <a name="remarks"></a>Comentarios

El  _parámetro pcb_ de la función **ScRelocNotifications** es opcional. 
  
## <a name="see-also"></a>Vea también



[ScRelocProps](screlocprops.md)

