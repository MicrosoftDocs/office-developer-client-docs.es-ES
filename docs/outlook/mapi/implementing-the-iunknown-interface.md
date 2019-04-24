---
title: Implementación de la interfaz IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310048"
---
# <a name="implementing-the-iunknown-interface"></a>Implementación de la interfaz IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los métodos de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , que se implementan en cada objeto MAPI, admiten la comunicación entre objetos y la administración de objetos. 
  
 **IUnknown** tiene tres métodos: [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** habilita un objeto para determinar si otro objeto admite una interfaz determinada. Con **QueryInterface**, se puede interactuar con dos objetos que no tienen conocimientos previos sobre la funcionalidad de los demás. Si el objeto que implementa **QueryInterface** admite la interfaz en cuestión, devuelve un puntero a la implementación de la interfaz. Si el objeto no admite la interfaz solicitada, devuelve el valor MAPI_E_INTERFACE_NOT_SUPPORTED. 
  
Cuando **QueryInterface** devuelve un puntero de interfaz solicitada, también debe aumentar el recuento de referencia del nuevo objeto. El recuento de referencia de un objeto es un valor numérico que se usa para administrar la duración del objeto. Cuando el recuento de referencias es mayor que 1, la memoria del objeto no se puede liberar porque se está usando de forma activa. Solo cuando el recuento de referencia cae a 0, el objeto puede liberarse de forma segura. 
  
Los otros dos métodos **IUnknown** , **AddRef** y **Release**, administran el recuento de referencia. **AddRef** incrementa el recuento de referencias, mientras que **Release** lo reduce. Todos los métodos o funciones de la API que devuelven punteros de interfaz, como **QueryInterface**, deben llamar a **AddRef** para incrementar el recuento de referencia. Todas las implementaciones de los métodos que reciben punteros de interfaz deben llamar a **Release** para disminuir el recuento cuando el puntero ya no es necesario. La **versión** comprueba un recuento de referencias existente, liberando la memoria asociada a la interfaz sólo si el recuento es 0. 
  
> [!NOTE]
> Dado que no se requiere **AddRef** y **Release** para devolver valores precisos, los llamadores de estos métodos no deben usar los valores devueltos para determinar si un objeto sigue siendo válido o se ha destruido. 
  
## <a name="see-also"></a>Vea también



[Implementación de objetos MAPI](implementing-mapi-objects.md)

