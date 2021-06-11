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
  
Los métodos de la [interfaz IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) implementados en cada objeto MAPI, admiten la comunicación entre objetos y la administración de objetos. 
  
 **IUnknown** tiene tres métodos: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)y [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** permite que un objeto determine si otro objeto admite una interfaz determinada. Con **QueryInterface,** pueden interactuar dos objetos sin conocimientos previos de la funcionalidad del otro. Si el objeto que implementa **QueryInterface** admite la interfaz en cuestión, devuelve un puntero a la implementación de la interfaz. Si el objeto no admite la interfaz solicitada, devuelve el MAPI_E_INTERFACE_NOT_SUPPORTED valor. 
  
Cuando **QueryInterface** devuelve un puntero de interfaz solicitado, también debe aumentar el recuento de referencias del nuevo objeto. El recuento de referencias de un objeto es un valor numérico que se usa para administrar la duración del objeto. Cuando el recuento de referencias es mayor que 1, la memoria del objeto no se puede liberar porque se está utilizando activamente. Solo cuando el recuento de referencias cae a 0, el objeto se puede liberar de forma segura. 
  
Los otros dos **métodos IUnknown,** **AddRef** y **Release,** administran el recuento de referencias. **AddRef** incrementa el recuento de referencias, mientras **que Release** lo disminuye. Todos los métodos o funciones api que devuelven punteros de interfaz, como **QueryInterface**, deben llamar a **AddRef** para incrementar el recuento de referencias. Todas las implementaciones de métodos que reciben punteros de interfaz deben llamar a **Release** para disminuir el número cuando el puntero ya no sea necesario. **Libera** las comprobaciones de un recuento de referencias existente, liberando la memoria asociada a la interfaz solo si el recuento es 0. 
  
> [!NOTE]
> Dado **que AddRef** y **Release** no son necesarios para devolver valores precisos, los autores de llamadas de estos métodos no deben usar los valores devueltos para determinar si un objeto sigue siendo válido o si se ha destruido. 
  
## <a name="see-also"></a>Vea también



[Implementación de objetos MAPI](implementing-mapi-objects.md)

