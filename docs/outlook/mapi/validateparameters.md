---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425207"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llama a una función interna para comprobar los parámetros que las aplicaciones cliente han pasado a los proveedores de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parámetros

 _eMethod_
  
> a Especifica, por enumeración, el método que se va a validar. 
    
 _Primero_
  
> a Puntero al primer argumento de la pila.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Todos los parámetros son válidos. 
    
MAPI_E_CALL_FAILED 
  
> Uno o varios de los parámetros no son válidos.
    
## <a name="remarks"></a>Comentarios

La macro **ValidateParameters** se ha reemplazado por la macro [ValidateParms](validateparms.md) . **ValidateParameters** no funciona correctamente en plataformas RISC y ahora se impide su compilación en ellos. Sigue compilando y funciona correctamente en plataformas Intel, pero **ValidateParms** se recomienda en todas las plataformas. 
  

