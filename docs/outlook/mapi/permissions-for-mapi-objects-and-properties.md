---
title: Permisos para objetos MAPI y propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: aad19bbc016af6bdc0b17124b46112656af53a4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818470"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Permisos para objetos MAPI y propiedades

  
  
**Hace referencia a**: Outlook 
  
Permiso de acceso o el conjunto de operaciones de permisible, puede ser una característica de objetos MAPI y de las propiedades individuales compatibles con esos objetos. Acceso a objetos está determinada por el elemento primario de un objeto. Para un mensaje, su carpeta determina los permisos de acceso. Para un usuario de mensajería o lista de distribución, su contenedor de la libreta de direcciones realiza esta determinación. Cuando un objeto como un mensaje reside en dos carpetas, los permisos para las dos copias del objeto pueden ser diferentes. 
  
Los clientes con estos objetos pueden solicitar el mayor nivel de acceso permitido para el objeto estableciendo el indicador MAPI_BEST_ACCESS en la llamada [IMAPISession::OpenEntry](imapisession-openentry.md) . Dependiendo del proveedor de servicio que se implementa el objeto, el cliente puede o no puede tener el nivel de acceso necesario. Los clientes pueden determinar el nivel de acceso que se hayan concedido mediante una llamada al método **GetProps** para recuperar la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) del objeto. Sin embargo, debido a que el proveedor de servicios debe generar dinámicamente el valor de esta propiedad, se recomienda que los clientes recuperan sólo cuando sea necesario. 
  
Para determinar si permite la modificación de un contenedor, como una carpeta, un contenedor de la libreta de direcciones o una lista de distribución, llame a su método **GetProps** para recuperar la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)). Nivel de acceso de contenedor afecta a los clientes en cuanto a cómo se visualizan sus interfaces de usuario. También afecta a los implementadores de objetos dentro de los contenedores en términos de su para mostrar la interfaz de usuario y su implementación general. 
  
Acceso a una propiedad determinada está determinado por el esquema de propiedad configurar MAPI para el objeto que posee la propiedad. Esquemas de propiedad especifican el conjunto de propiedades opcionales y obligatorios para un objeto y sus permisos de acceso. A diferencia de acceso a los objetos está determinada por primario el objeto, el acceso a la propiedad es global. Cada objeto, independientemente de los requisitos de acceso de primario del objeto, tiene los mismos permisos para la propiedad según lo determinado por el esquema.
  
Cuando una propiedad es de sólo lectura, siempre estará disponible con una llamada **GetProps** o **OpenProperty** . Sin embargo, dependiendo de la implementación del objeto compatible con la propiedad, existen dos resultados posibles para el método **SetProps** para modificar una propiedad y el método **DeleteProps** para quitarlo: 
  
- Producirá un error y devolver MAPI_E_NO_ACCESS
    
- Se realizan con éxito sin ninguna acción
    
Acceso de propiedad y el objeto también puede se recuperarán o establecerán mediante la interfaz [IPropData](ipropdataimapiprop.md) que hereda de la interfaz **IMAPIProp** . MAPI proporciona una implementación de **IPropData** que se basa en datos en la memoria. Proveedores de servicios pueden utilizar **IPropData** para implementar **IMAPIProp** en determinadas circunstancias, como para su objeto de estado o si están utilizando una base de datos que no tiene transacciones integradas. **IPropData** funciona exclusivamente en la memoria, haciendo que sea innecesario bloquear y desbloquear los datos. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

