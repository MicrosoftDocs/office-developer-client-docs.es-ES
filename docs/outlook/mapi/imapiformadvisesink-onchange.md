---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 01bdf6cdde864d1ea4ed19dfeb01a96236dc9c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817268"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Se aplica a**: Outlook 
  
Indica que se ha producido un cambio en el estado del Visor del formulario. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Sintaxis

 _ulDir_
  
> [entrada] Una máscara de bits de indicadores que proporciona información sobre el cambio que se ha producido en el Visor y la respuesta esperada en el formulario. Se pueden establecer los siguientes indicadores:
    
VCSTATUS_CATEGORY 
  
> Hay un mensaje siguiente o anterior en otra categoría. 
    
VCSTATUS_INTERACTIVE 
  
> El formulario debe mostrar una interfaz de usuario. Si no se establece este indicador, el formulario debe suprimir mostrar la interfaz de usuario, incluso en respuesta a un verbo que normalmente hace que una interfaz de usuario que se mostrará. 
    
VCSTATUS_MODAL 
  
> El formulario es modal en el Visor de formulario. 
    
VCSTATUS_NEXT 
  
> Hay un mensaje siguiente en el Visor de formulario. 
    
VCSTATUS_PREV 
  
> Hay un mensaje anterior en el Visor de formulario. 
    
VCSTATUS_READONLY 
  
> Eliminar, enviar y mover las operaciones deben deshabilitarse. 
    
VCSTATUS_UNREAD 
  
> Hay un mensaje no leído siguiente o anterior en el Visor de formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación fue correcta.
    
## <a name="remarks"></a>Notas

Visores de formulario llamar al método **IMAPIFormAdviseSink::OnChange** para notificar el formulario acerca de un cambio en el estado de un visor. Normalmente, el único cambio es activando o desactivando la marca VCSTATUS_NEXT o VCSTATUS_PREVIOUS en función de la presencia o ausencia de un mensaje siguiente o anterior en el Visor. Por lo tanto, el objeto de formulario, a continuación, habilita o deshabilita cualquier acciones siguiente o anteriores que admite. 
  
No se puede cambiar la configuración de VCSTATUS_MODAL y VCSTATUS_INTERACTIVE en un contexto de vista después de que se han creado.
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

La implementación específica de este método depende completamente de las características específicas del formulario. La mayoría de los objetos de formulario use este método para cambiar la interfaz de usuario (por ejemplo, para habilitar o deshabilitar comandos de menú o botones para que coincida con el parámetro de indicadores de estado de Visor).
  
## <a name="see-also"></a>Ver también



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md)

