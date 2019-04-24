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
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360497"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llama a una función interna para comprobar los parámetros que las aplicaciones cliente han pasado a los proveedores de servicios y MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT UlValidateParms(
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
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error impidió que se completara la operación.
    
## <a name="remarks"></a>Comentarios

Se supone que los parámetros que se han pasado entre MAPI y los proveedores de servicios son correctos y solo se someten a la validación de depuración con la macro [CheckParms](checkparms.md) . Los proveedores deben comprobar todos los parámetros pasados por las aplicaciones cliente, pero los clientes deben suponer que los parámetros MAPI y del proveedor son correctos. Use la macro **HR_FAILED** para probar los valores devueltos. 
  
Se llama a la macro **UlValidateParms** de forma diferente en función de si el código de llamada es C o C++. Esta macro se usa para validar los parámetros de los métodos **IUnknown** y MAPI que devuelven valores ulong en lugar de HRESULT; la macro [ValidateParms](validateparms.md) funciona para todos los demás. 
  

