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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315298"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona una forma alternativa para invocar el método OLE **IUnknown:: Release**. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Parameters

 _punk_
  
> a Puntero a una interfaz derivada de la interfaz **IUnknown** , en otras palabras, cualquier interfaz MAPI. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen inesperado o desconocido impidió que se completara la operación.
    
## <a name="remarks"></a>Comentarios

El recuento de referencia es el número de punteros existentes en el objeto que se va a liberar. 
  
Si el parámetro _punk_ es null, la función regresa inmediatamente sin llamar a **IUnknown:: Release**
  
 **UlRelease** devuelve el valor devuelto por el método **IUnknown:: Release** , que puede ser igual que el recuento de referencias para el objeto que se va a liberar. 
  
Para obtener más información acerca de **IUnknown:: Release**, vea [implementar la interfaz IUnknown](implementing-the-iunknown-interface.md). 
  

