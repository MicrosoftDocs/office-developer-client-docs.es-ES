---
title: Utilizar objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d732efe5276f4756f43b4aca46e1c33d6f103844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329683"
---
# <a name="using-mapi-objects"></a>Utilizar objetos MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes y proveedores de servicios usan objetos MAPI llamando a los métodos en sus implementaciones de interfaz. Esta es la única forma en que se pueden usar objetos MAPI; que se implementan mediante un objeto fuera de una interfaz MAPI no son accesibles públicamente. Dado que todas las interfaces de un objeto están relacionadas a través de la herencia, el usuario de un objeto puede llamar a métodos en la interfaz base o en una de las interfaces heredadas como si pertenezcan a la misma interfaz. 
  
Cuando un usuario de un objeto desea realizar una llamada a un método y ese objeto implementa varias interfaces relacionadas con la herencia, el usuario no necesita saber a qué interfaz pertenece el método. El usuario puede llamar a cualquiera de los métodos en cualquiera de las interfaces con un solo puntero al objeto. Por ejemplo, la siguiente ilustración muestra cómo una aplicación cliente usa un objeto de carpeta. Los objetos Folder implementan la interfaz [IMAPIFolder : IMAPIContainer,](imapifolderimapicontainer.md) que hereda de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indirectamente a través de [IMAPIProp : IUnknown](imapipropiunknown.md) e [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). Un cliente puede llamar a uno de los métodos **IMAPIProp,** como [IMAPIProp::GetProps,](imapiprop-getprops.md)y uno de los métodos [IMAPIFolder : IMAPIContainer,](imapifolderimapicontainer.md) como [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), de la misma manera con el mismo puntero de objeto. Un cliente no es consciente o afectado por el hecho de que estas llamadas pertenecen a interfaces diferentes.
  
**Uso de cliente de un objeto de carpeta**
  
![Uso de cliente de un objeto de carpeta]Uso de cliente de un objeto de(media/amapi_40.gif "carpeta")
  
Estas llamadas se traducen en código de forma diferente en función de si el cliente que realiza las llamadas se escribe en C o C++. Para poder realizar cualquier llamada a un método, se debe recuperar un puntero a la implementación de la interfaz. Los punteros de interfaz se pueden obtener de las siguientes maneras:
  
- Llamar a un método en un objeto diferente.
    
- Llamar a una función api.
    
- Llamar al [método IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) en el objeto de destino. 
    
MAPI proporciona varios métodos y funciones api que devuelven punteros a las implementaciones de la interfaz. Por ejemplo, los clientes pueden llamar al método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para recuperar un puntero a un objeto de tabla que proporciona acceso a la información del proveedor del almacén de mensajes a través de la interfaz [IMAPITable : IUnknown.](imapitableiunknown.md) Los proveedores de servicios pueden llamar a la función DE API [CreateTable](createtable.md) para recuperar un puntero a un objeto de datos de tabla. Cuando no hay ninguna función o método disponible y los clientes o proveedores de servicios ya tienen un puntero a un objeto, pueden llamar al método **QueryInterface** del objeto para recuperar un puntero a otra de las implementaciones de la interfaz del objeto. 
  
## <a name="see-also"></a>Consulte también

- [Información general sobre el objeto MAPI y la interfaz](mapi-object-and-interface-overview.md)

