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
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428189"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada que llama MAPI cuando ha descartado un cuadro de diálogo de libreta de direcciones de modeless. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Función definida implementada por:  <br/> |Aplicaciones cliente  <br/> |
|Función definida llamada por:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Valor específico de la implementación que normalmente se usa para pasar información de la interfaz de usuario a una función. Por ejemplo, en Microsoft Windows este parámetro es el identificador de ventana principal del cuadro de diálogo y es de tipo HWND, que se convierte en un **ULONG_PTR**. Un valor de cero indica que no hay ninguna ventana primaria. 
    
 _lpvContext_
  
> [in] Puntero a un valor arbitrario pasado a la función de devolución de llamada cuando MAPI lo llama. Este valor puede representar una dirección de importancia para la aplicación cliente. Normalmente, para el código C++,  _lpvContext_ es un puntero a la dirección de una instancia de objeto de C++. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno
  
## <a name="remarks"></a>Comentarios

Cuando la aplicación cliente invoca un cuadro de diálogo de libreta de direcciones de modeless, incluye en su bucle de mensaje de Windows una llamada a una función basada en el prototipo [ACCELERATEABSDI,](accelerateabsdi.md) que comprueba y procesa las teclas de aceleración. Cuando se cierra el cuadro de diálogo, MAPI llama a la función basada **en DISMISSMODELESS** para que la aplicación cliente deje de llamar a la función basada en **ACCELERATEABSDI.** 
  
## <a name="see-also"></a>Vea también



[ADRPARM](adrparm.md)

