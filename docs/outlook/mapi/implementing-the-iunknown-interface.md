---
title: Implementar la interfaz IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f9ab3b75743d882aca0145b73b8ef707204cc8de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571902"
---
# <a name="implementing-the-iunknown-interface"></a>Implementar la interfaz IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los métodos de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) , implementada en cada objeto MAPI, admiten la administración de comunicación y objeto entre. 
  
 **IUnknown** tiene tres métodos: [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)e [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** permite a un objeto determinar si otro objeto admite una interfaz determinada. Con **QueryInterface**, pueden interactuar dos objetos sin conocimiento previo de la funcionalidad del otro. Si el objeto que implementa **QueryInterface** es compatible con la interfaz en cuestión, devuelve un puntero a la implementación de la interfaz. Si el objeto no admite la interfaz solicitada, devuelve el valor MAPI_E_INTERFACE_NOT_SUPPORTED. 
  
Cuando **QueryInterface** devuelve un puntero de interfaz solicitada, también debe aumentar el recuento de referencia del nuevo objeto. Recuento de referencia de un objeto es un valor numérico que se usa para administrar el ciclo de vida del objeto. Cuando el recuento de referencia es mayor que 1, la memoria del objeto no se puede liberar porque se usa activamente. Es solo cuando el recuento de referencia cae a 0 que el objeto puede liberarse de forma segura. 
  
Los otros dos métodos **IUnknown** , **AddRef** y **Release**, administran el recuento de referencia. **AddRef** se incrementa el recuento de referencia, mientras se disminuye **versión** lo. Todos los métodos o funciones de la API que devuelven punteros a la interfaz, como **QueryInterface**, deben llamar a **AddRef** para incrementar el recuento de referencia. Todas las implementaciones de los métodos que reciben punteros a la interfaz deben llamar a **Release** para disminuir el recuento cuando el puntero ya no es necesario. **Versión** se comprueba para un recuento de referencia existente, liberar la memoria asociada con la interfaz sólo si el recuento es 0. 
  
> [!NOTE]
> Debido a que no están necesario **AddRef** y **Release** para devolver valores precisos, los autores de llamadas de estos métodos no deben utilizar los valores devueltos para determinar si un objeto todavía es válido o se destruye. 
  
## <a name="see-also"></a>Recursos adicionales



[Implementar objetos MAPI](implementing-mapi-objects.md)

