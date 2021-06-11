---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415848"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona una forma alternativa de invocar el método OLE **IUnknown::Release**. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Parameters

 _punk_
  
> [in] Puntero a una interfaz derivada de la **interfaz IUnknown,** es decir, cualquier interfaz MAPI. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen inesperado o desconocido impidió que se completara la operación.
    
## <a name="remarks"></a>Comentarios

El recuento de referencias es el número de punteros existentes al objeto que se va a liberar. 
  
Si el  _parámetro punk_ es NULL, la función devuelve inmediatamente sin llamar a **IUnknown::Release**
  
 **UlRelease devuelve** el valor devuelto por el método **IUnknown::Release,** que puede ser igual al recuento de referencias para el objeto que se va a liberar. 
  
Para obtener más información **acerca de IUnknown::Release,** vea [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md). 
  

