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
ms.openlocfilehash: 195a82bfcc163ee01d2d42c71e79a8f5c9c620e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564636"
---
# <a name="form-states"></a>Estados de formulario

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Objetos de formulario pueden estar en uno de cinco estados distintos, dependiendo de qué se ha llamado a los métodos en ellos y si los errores se han producido en la realización de estos métodos. Los Estados se describen en los temas siguientes:
  
- [Estado sin inicializar](uninitialized-state.md)
    
- [Estado normal](normal-state.md)
    
- [Estado NoScribble](noscribble-state.md)
    
- [Estado HandsOffAfterSave](handsoffaftersave-state.md)
    
- [Estado HandsOffFromNormal](handsofffromnormal-state.md)
    
Los Estados principalmente se relacionan con el estado de los datos en el objeto de formulario. Los distintos Estados reflejan si los datos se deben guardar, si el objeto de formulario debe permitir que las modificaciones realizadas en los datos y qué punto en el proceso de guardar los datos que el formulario está en. Por lo tanto, el formulario Estados y transiciones entre ellas tienen mucho más relacionada con la implementación del servidor de su formulario de [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos que cualquier otro de la interfaz. Conocimiento de estos Estados es muy útil para la correcta ejecución de las interfaces de formulario MAPI que debe implementar el servidor de formulario. 
  
En los temas de esta sección se describen los distintos Estados, junto con las acciones permitidas que causar transiciones a otros Estados. No se permiten las transiciones no aparece en los temas. Si los objetos de formulario realizar transiciones no permitidas entre Estados, no se comportará de las maneras en que los clientes de mensajería esperan y podrían causar un comportamiento inesperado objeto cliente o formulario.
  
> [!NOTE]
> Algunas transiciones de estado dependen de la información de estados anteriores. El servidor de formulario muy probable que deba implementar un indicador en sus objetos de formulario para indicar si han cambiado los valores de las propiedades del mensaje para facilitar los cambios de estado de una versión posterior. 
  
## <a name="see-also"></a>Recursos adicionales

- [Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

