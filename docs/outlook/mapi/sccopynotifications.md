---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 28a802ffc43b08d3e2ec2be26dd98fa78f474d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820565"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Se aplica a**: Outlook 
  
Copia un grupo de las notificaciones de eventos en un único bloque de memoria. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Sintaxis

 _cntf_
  
> [entrada] Recuento de las estructuras de [notificación](notification.md) en la matriz indicada por el parámetro _rgntf_ . 
    
 _rgntf_
  
> [entrada] Puntero a una matriz de las estructuras de **notificación** para definir las notificaciones de eventos que se va a copiar. 
    
 _pvDst_
  
> [out] Puntero a las notificaciones devueltas. 
    
 _placa de circuitos impresos_
  
> [out] Se almacena un puntero opcional a una variable donde el tamaño, en bytes, de la matriz indicado por el parámetro _rgntf_ . Si no es NULL, el parámetro _pcb_ se establece en el número de bytes que se almacenan en el parámetro _pvDst_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Las notificaciones de eventos se copiaron correctamente.
    
E_INVALIDARG
  
> Se ha producido una notificación no válida.
    
## <a name="remarks"></a>Notas

Si se pasa NULL en el parámetro de la _placa de circuitos impresos_ , no copiar se lleva a cabo; Si se pasa un valor no nulo en _placa de circuitos impresos_, la función **ScCopyNotifications** copia el tamaño de la matriz y la matriz de sí mismo en un único bloque de memoria. Si la _placa de circuitos impresos_ no es NULL, se establece el número de bytes que se almacenan en el parámetro _pvDst_ . El parámetro _pvDst_ debe ser lo suficientemente grande como para contener toda la matriz. 
  

