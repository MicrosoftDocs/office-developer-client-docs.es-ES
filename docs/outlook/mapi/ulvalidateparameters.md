---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431277"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llama a una función interna para comprobar los parámetros que las aplicaciones cliente han pasado a los proveedores de servicios y MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parámetros

 _eMethod_
  
> [entrada] Especifica, por enumeración, el método que se debe validar. 
    
 _Primero_
  
> [entrada] Puntero al primer argumento de la pila.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen inesperado o desconocido impidió que se completara la operación.
    
## <a name="remarks"></a>Comentarios

La macro **UlValidateParameters** ha sido reemplazada por la macro [UlValidateParms.](ulvalidateparms.md) **UlValidateParameters** no funciona correctamente en plataformas RISC y ahora no se puede compilar en ellas. Sigue compilando y funciona correctamente en plataformas Intel, pero se recomienda **UlValidateParms** en todas las plataformas. 
  

