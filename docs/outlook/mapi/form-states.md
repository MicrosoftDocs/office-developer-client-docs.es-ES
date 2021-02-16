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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429169"
---
# <a name="form-states"></a>Estados de formulario

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los objetos de formulario pueden estar en uno de los cinco estados distintos, dependiendo de los métodos que se hayan llamado en ellos y de si se han producido errores al realizar esos métodos. Los estados se describen en los siguientes temas:
  
- [Estado no inicializado](uninitialized-state.md)
    
- [Estado normal](normal-state.md)
    
- [Estado no se puede suscribir](noscribble-state.md)
    
- [Estado HandsOffAfterSave](handsoffaftersave-state.md)
    
- [Estado HandsOffFromNormal](handsofffromnormal-state.md)
    
Los estados se relacionan principalmente con el estado de los datos del objeto de formulario. Los distintos estados reflejan si los datos deben guardarse, si el objeto de formulario debe permitir modificaciones en los datos y en qué punto del proceso de guardar los datos en los que se encuentra el formulario. Como tal, los estados de formulario y las transiciones entre ellos tienen más que ver con la implementación del servidor de formulario de métodos de interfaz [IPersistMessage : IUnknown](ipersistmessageiunknown.md) que cualquier otro. El conocimiento de estos estados es muy útil para la correcta implementación de las interfaces de formulario MAPI que debe implementar el servidor de formularios. 
  
En los temas de esta sección se describen los distintos estados, junto con las acciones permitidas que provocan transiciones a otros estados. No se permiten las transiciones que no aparecen en los temas. Si los objetos de formulario hacen transiciones no permitidos entre estados, no se comportarán de la forma esperada por los clientes de mensajería y podrían provocar un comportamiento impredecible de los objetos de formulario o cliente.
  
> [!NOTE]
> Algunas transiciones de estado dependen de la información de estados anteriores. Lo más probable es que el servidor de formulario tenga que implementar una marca en sus objetos de formulario para indicar si los valores de las propiedades del mensaje se han cambiado para facilitar cambios de estado posteriores. 
  
## <a name="see-also"></a>Consulte también

- [Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md)

