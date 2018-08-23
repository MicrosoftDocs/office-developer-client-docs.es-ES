---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d5cb43bfa3acd912e397644657223c177d6afb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589325"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un objeto de receptor advise, dado un contexto especificado por la implementación de llamada y una función de devolución de llamada que se desencadene mediante una notificación de eventos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parámetros

 _lpfnCallback_
  
> [entrada] Puntero a una función de devolución de llamada según el prototipo [NOTIFCALLBACK](notifcallback.md) es MAPI que se llama cuando se produce un evento de notificación para el recién creada de aviso receptor. 
    
 _lpvContext_
  
> [entrada] Puntero a los datos del autor de la llamada se pasa a la función de devolución de llamada cuando llama a MAPI. Los datos del autor de la llamada pueden representar una dirección de cifra significativa para el cliente o el proveedor. Normalmente, para el código de C++, el parámetro _lpvContext_ representa un puntero a la dirección de un objeto. 
    
 _lppAdviseSink_
  
> [out] Puntero a un puntero a un objeto de receptor advise.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Para usar la función **HrAllocAdviseSink** , una aplicación de cliente o un proveedor de servicios crea un objeto para recibir notificaciones, crea una función de devolución de llamada de notificación según el prototipo de función [NOTIFCALLBACK](notifcallback.md) que va asociado con ese objeto y pasa un puntero al objeto en la función **HrAllocAdviseSink** como el valor de _lpvContext_ . Al hacerlo, realiza una notificación; y como parte del proceso de notificación, llama a la función de devolución de llamada con el puntero de objeto como el contexto de MAPI. 
  
MAPI implementa su motor de notificación de forma asincrónica. En C++, la devolución de llamada de notificación puede ser un método de objeto. Si el objeto generación de la notificación no está presente, el cliente o proveedor que solicita notificación debe mantener un recuento de referencia independiente para ese objeto para el objeto de aviso receptor. 
  
> [!CAUTION]
> **HrAllocAdviseSink** debe usarse con moderación; es más seguro para los clientes crear sus propios receptores advise. 
  

