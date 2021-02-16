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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437997"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina el tamaño, en bytes, de una matriz de notificaciones de eventos y valida la memoria asociada a la matriz.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parámetros

 _cntf_
  
> [entrada] Recuento de [estructuras notification](notification.md) en la matriz indicada por el _parámetro rgntf._ 
    
 _rgntf_
  
> [entrada] Puntero a la matriz de **estructuras notification** cuyo tamaño se va a determinar. 
    
 _indeste_
  
> [salida] Puntero opcional al tamaño, en bytes, de la matriz a la que apunta el _parámetro rgntf._ Si es NULL, **ScCountNotifications** valida la matriz de notificaciones. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El recuento se determinó correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Se encontró una notificación no válida.
    
## <a name="remarks"></a>Comentarios

Si se pasa NULL en el parámetro _de botón,_ la función **ScCountNotifications** solo valida la matriz de notificaciones, pero no se realiza ningún recuento; si se pasa un valor que no es nulo en lugar de _bytes_, **ScCountNotifications** determina el tamaño de la matriz y almacena la _causa._ El  _parámetrodimensional_ debe ser lo suficientemente grande como para contener toda la matriz. 
  

