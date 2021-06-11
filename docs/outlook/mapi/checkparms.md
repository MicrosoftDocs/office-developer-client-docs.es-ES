---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422281"
---
# <a name="checkparms"></a>CheckParms

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llama a una función interna para validar parámetros de depuración en métodos de proveedor de servicios a los que llama MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parámetros

 _eMethod_
  
> [in] Especifica, por enumeración, el método que se debe validar. 
    
 _Primero_
  
> [in] Puntero al primer argumento de la pila.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada ha sido correcta.
    
## <a name="remarks"></a>Comentarios

A diferencia de las macros [ValidateParms](validateparms.md) y [UlValidateParms,](ulvalidateparms.md) la macro **CheckParms** no realiza una validación completa de parámetros. Se supone que los parámetros pasados entre MAPI y los proveedores de servicios son correctos, por lo que **CheckParms** solo realiza una validación de depuración. 
  

