---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c66ff2338eb5751dbffe392a6a26258fb1c89476
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565840"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada que llama MAPI cuando ha descartado un cuadro de diálogo de la libreta de direcciones no modal. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Función definido implementada por:  <br/> |Aplicaciones cliente  <br/> |
|Llamado por una función definida:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Un valor específico de la implementación suele utilizado para pasar información de interfaz de usuario a una función. Por ejemplo, en Microsoft Windows en este parámetro es el identificador de ventana primario para el cuadro de diálogo y es de tipo HWND, que se convierte en un **ULONG_PTR**. Un valor de cero indica que no hay ninguna ventana primaria. 
    
 _lpvContext_
  
> [entrada] Puntero a un valor arbitrario se pasa a la función de devolución de llamada cuando llama a MAPI. Este valor puede representar una dirección de importancia a la aplicación cliente. Normalmente, para el código de C++, _lpvContext_ es un puntero a la dirección de una instancia de objeto de C++. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno
  
## <a name="remarks"></a>Observaciones

Cuando la aplicación cliente invoca un cuadro de diálogo de la libreta de direcciones no modal, en el bucle de mensajes de Windows incluye una llamada a una función según el prototipo [ACCELERATEABSDI](accelerateabsdi.md) , que busca y procesa las teclas de aceleración. Cuando se cierra el cuadro de diálogo, el **DISMISSMODELESS** en la función de función para que la aplicación cliente se detendrá al llamar a la **ACCELERATEABSDI** de las llamadas MAPI en función (función). 
  
## <a name="see-also"></a>Recursos adicionales



[ADRPARM](adrparm.md)

