---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433398"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llama a una función interna para validar parámetros de depuración en métodos de proveedor de servicios a los que llama MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT CheckParameters(
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

La **macro CheckParameters** ha sido reemplazada por la macro [CheckParms.](checkparms.md) **CheckParms** se recomienda en todas las plataformas. 
  

