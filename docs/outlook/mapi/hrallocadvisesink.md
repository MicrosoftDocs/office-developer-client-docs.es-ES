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
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428903"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un objeto de receptor de notificaciones, dado un contexto especificado por la implementación de llamada y una función de devolución de llamada que se desencadenará mediante una notificación de evento. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameters

 _lpfnCallback_
  
> a Puntero a una función de devolución de llamada basada en el prototipo [NOTIFCALLBACK](notifcallback.md) al que MAPI debe llamar cuando se produce un evento de notificación para el receptor de notificaciones recién creado. 
    
 _lpvContext_
  
> a Puntero a los datos del autor de la llamada pasados a la función de devolución de llamada cuando MAPI los llama. Los datos del autor de la llamada pueden representar una dirección de importancia para el cliente o el proveedor. Normalmente, para código de C++, el parámetro _lpvContext_ representa un puntero a la dirección de un objeto. 
    
 _lppAdviseSink_
  
> contempla Puntero a un puntero a un objeto de receptor de notificaciones.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Para usar la función **HrAllocAdviseSink** , una aplicación cliente o un proveedor de servicios crea un objeto para recibir notificaciones, crea una función de devolución de llamada de notificación basada en el prototipo de función [NOTIFCALLBACK](notifcallback.md) que va con ese objeto, y pasa un puntero al objeto en la función **HrAllocAdviseSink** como el valor _lpvContext_ . Al hacerlo, se realiza una notificación; como parte del proceso de notificación, MAPI llama a la función de devolución de llamada con el puntero del objeto como contexto. 
  
MAPI implementa su motor de notificación de forma asincrónica. En C++, la devolución de llamada de la notificación puede ser un método de objeto. Si el objeto que genera la notificación no está presente, el cliente o proveedor que solicita la notificación debe mantener un recuento de referencia independiente para ese objeto para el receptor de notificaciones del objeto. 
  
> [!CAUTION]
> **HrAllocAdviseSink** debe usarse con moderación; es más seguro para los clientes crear sus propios receptores de notificaciones. 
  

