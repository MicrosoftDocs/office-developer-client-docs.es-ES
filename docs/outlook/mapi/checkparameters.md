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
ms.openlocfilehash: a693c06d933c7e93d384aac8da8d5311eaf1d9da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816569"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**Hace referencia a**: Outlook 
  
Llama a una función interna para validar parámetros de depuración en los métodos de proveedor de servicio llamados por MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT CheckParameters(
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
  
> La llamada ha sido correcta.
    
## <a name="remarks"></a>Comentarios

La macro **CheckParameters** se ha sustituido por la macro [CheckParms](checkparms.md) . Se recomienda **CheckParms** en todas las plataformas. 
  

