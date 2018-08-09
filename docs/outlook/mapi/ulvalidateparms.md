---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 12b1655b1e6786d2ebc985e834b635679e59f7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820920"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**Hace referencia a**: Outlook 
  
Llama a una función interna para comprobar si que las aplicaciones cliente de los parámetros han pasado a proveedores de servicios y MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT UlValidateParms(
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
  
> Un error no puede completar la operación.
    
## <a name="remarks"></a>Comentarios

Parámetros pasados entre MAPI y servicio proveedores se supone que sea correcta y se sincronizan sólo depuración validación con la macro [CheckParms](checkparms.md) . Proveedores deben comprobar todos los parámetros que se pasó por las aplicaciones cliente, pero los clientes deben se presupone que MAPI y proveedor de parámetros correctos. Use la macro **HR_FAILED** para comprobar los valores devueltos. 
  
La macro **UlValidateParms** se llama de manera diferente dependiendo de si el código de llamada es C o C++. Esta macro se usa para validar los parámetros de los métodos de **IUnknown** y MAPI pocos que devuelven ULONG en lugar de los valores HRESULT; la macro [ValidateParms](validateparms.md) funciona para todos los demás. 
  

