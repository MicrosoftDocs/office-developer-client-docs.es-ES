---
title: Permisos para objetos y propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4efa9cd1596cffe19a19a62059f81fa553343d77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436177"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Permisos para objetos y propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El permiso de acceso, o el conjunto de operaciones permisivas, puede ser una característica de los objetos MAPI y de las propiedades individuales admitidas por dichos objetos. El acceso a objetos está determinado por el elemento primario de un objeto. Para un mensaje, su carpeta determina los permisos de acceso. Para un usuario de mensajería o una lista de distribución, su contenedor de libreta de direcciones realiza esta determinación. Cuando un objeto como un mensaje reside en dos carpetas, los permisos para las dos copias del objeto pueden ser diferentes. 
  
Los clientes que usan estos objetos pueden solicitar el máximo nivel de acceso permitido para el objeto mediante la configuración de la marca MAPI_BEST_ACCESS en la llamada [IMAPISession:: OpenEntry](imapisession-openentry.md) . Según el proveedor de servicios que implemente el objeto, es posible que el cliente no conceda el nivel de acceso necesario. Los clientes pueden determinar el nivel de acceso que se les ha concedido al llamar al método **GetProps** del objeto para recuperar la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)). Sin embargo, como el proveedor de servicios debe generar dinámicamente el valor de esta propiedad, se recomienda que los clientes lo recuperen solo cuando sea necesario. 
  
Para determinar si un contenedor, como una carpeta, un contenedor de libreta de direcciones o una lista de distribución permite la modificación, llame a su método **GetProps** para recuperar la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)). El acceso a nivel de contenedor afecta a los clientes en cuanto a cómo muestran sus interfaces de usuario. También afecta a los implementadores de objetos dentro de contenedores en términos de la visualización de la interfaz de usuario y su implementación general. 
  
El acceso a una propiedad determinada se determina mediante el esquema de propiedad configurado por MAPI para el objeto que posee la propiedad. Los esquemas de propiedad especifican el conjunto de propiedades obligatorias y opcionales para un objeto y su permiso de acceso. A diferencia del acceso a objeto, que está determinada por el elemento principal del objeto, el acceso a la propiedad es global. Cada objeto, independientemente de los requisitos de acceso del elemento principal del objeto, tiene los mismos permisos para la propiedad que el esquema determinado.
  
Cuando una propiedad es de sólo lectura, siempre estará disponible con una llamada **GetProps** o **OpenProperty** . Sin embargo, en función de la implementación del objeto que admite la propiedad, hay dos posibles resultados para que el método **SetProps** para modificar una propiedad y el método **DeleteProps** para quitarlo: 
  
- Error y devolución MAPI_E_NO_ACCESS
    
- Correcto sin que se realice ninguna acción
    
El acceso a la propiedad y el objeto también se puede recuperar o establecer mediante la interfaz [IPropData](ipropdataimapiprop.md) que hereda de la interfaz **IMAPIProp** . MAPI proporciona una implementación de **IPropData** que se basa en los datos de la memoria. Los proveedores de servicios pueden usar **IPropData** para implementar **IMAPIProp** en determinadas circunstancias, como en su objeto de estado o si usan una base de datos que no tiene transacciones integradas. **IPropData** funciona exclusivamente en la memoria, lo que hace innecesaria la bloqueo y el desbloqueo de los datos. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

