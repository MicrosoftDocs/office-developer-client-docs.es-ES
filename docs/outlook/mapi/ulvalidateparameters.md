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
ms.openlocfilehash: 42b2f8e9695b1dbdc5ea02db5a4e8a0eaba6099c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820931"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**Hace referencia a**: Outlook 
  
Llama a una función interna para comprobar si que las aplicaciones cliente de los parámetros han pasado a proveedores de servicios y MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parámetros

 _eMethod_
  
> [entrada] Especifica el (enumeración), el método para validar. 
    
 _Primero_
  
> [entrada] Puntero al primer argumento en la pila.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen desconocido o inesperado no puede completar la operación.
    
## <a name="remarks"></a>Comentarios

La macro **UlValidateParameters** se ha sustituido por la macro [UlValidateParms](ulvalidateparms.md) . **UlValidateParameters** no funciona correctamente en plataformas RISC y ahora no puede compilar en ellos. Aún compila y funciona correctamente en plataformas Intel, pero se recomienda **UlValidateParms** en todas las plataformas. 
  

