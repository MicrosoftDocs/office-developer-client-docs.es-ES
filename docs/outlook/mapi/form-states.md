---
title: Estados de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327520"
---
# <a name="form-states"></a>Estados de formulario

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los objetos de formulario pueden estar en uno de cinco Estados distintos, en función de los métodos a los que se haya llamado y si se han producido errores en la realización de esos métodos. Los Estados se describen en los siguientes temas:
  
- [Estado sin inicializar](uninitialized-state.md)
    
- [Estado normal](normal-state.md)
    
- [Estado noScribble](noscribble-state.md)
    
- [Estado HandsOffAfterSave](handsoffaftersave-state.md)
    
- [Estado HandsOffFromNormal](handsofffromnormal-state.md)
    
Los Estados están principalmente relacionados con el estado de los datos del objeto de formulario. Los diferentes Estados reflejan si es necesario guardar los datos, si el objeto de formulario debe permitir modificaciones a los datos y en qué punto del proceso se guardan los datos en el formulario. Por lo tanto, los Estados de formulario y las transiciones entre ellos tienen más que ver con la implementación del servidor de formularios de [IPersistMessage:](ipersistmessageiunknown.md) métodos de interfaz IUnknown que otros. Conocer estos Estados es muy útil para la correcta implementación de las interfaces de formulario MAPI que debe implementar su servidor de formularios. 
  
En los temas de esta sección se describen los distintos Estados, junto con las acciones permitidas que provocan transiciones a otros Estados. No se permiten las transiciones que no aparezcan en los temas. Si los objetos de formulario realizan transiciones entre Estados no permitidos, no se comportarán de la manera que esperan los clientes de mensajería y podrían provocar un comportamiento impredecible del cliente o del objeto de formulario.
  
> [!NOTE]
> Algunas transiciones de estado dependen de la información de los Estados anteriores. El servidor de formularios probablemente tendrá que implementar una marca en sus objetos de formulario para indicar si los valores de las propiedades del mensaje se han cambiado para facilitar los cambios de estado posteriores. 
  
## <a name="see-also"></a>Vea también

- [Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

