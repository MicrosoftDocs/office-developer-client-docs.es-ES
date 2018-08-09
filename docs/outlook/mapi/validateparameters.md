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
ms.openlocfilehash: 921417d8fc73ca9c1f126b2cb0add23f6625e3f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820970"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**Hace referencia a**: Outlook 
  
Llama a una función interna para comprobar si que las aplicaciones cliente de los parámetros han pasado a proveedores de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT ValidateParameters(
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
  
> Todos los parámetros son válidos. 
    
MAPI_E_CALL_FAILED 
  
> Uno o varios de los parámetros no son válidos.
    
## <a name="remarks"></a>Comentarios

La macro **ValidateParameters** se ha sustituido por la macro [ValidateParms](validateparms.md) . **ValidateParameters** no funciona correctamente en plataformas RISC y ahora no puede compilar en ellos. Aún compila y funciona correctamente en plataformas Intel, pero se recomienda **ValidateParms** en todas las plataformas. 
  

