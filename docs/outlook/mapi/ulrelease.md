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
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820922"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Hace referencia a**: Outlook 
  
Proporciona una manera alternativa para invocar el método OLE **IUnknown:: Release**. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Parámetros

 _pUnk_
  
> [entrada] Puntero a una interfaz derivada de la interfaz **IUnknown** , en otras palabras cualquier interfaz MAPI. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen desconocido o inesperado no puede completar la operación.
    
## <a name="remarks"></a>Comentarios

El recuento de referencia es el número de punteros existentes para el objeto que se va a liberar. 
  
Si el parámetro _punk_ es NULL, la función devuelve inmediatamente sin llamar a **IUnknown:: Release**
  
 **UlRelease** devuelve el valor devuelto por el método **IUnknown:: Release** , que puede ser igual que el recuento de referencia para el objeto que se va a liberar. 
  
Para obtener más información acerca de **IUnknown:: Release**, vea [implementación de la interfaz IUnknown](implementing-the-iunknown-interface.md). 
  

