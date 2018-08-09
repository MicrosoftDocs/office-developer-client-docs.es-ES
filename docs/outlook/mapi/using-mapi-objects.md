---
title: Uso de objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a355faf85a44f6257b77b7171aa965faabf57fe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820964"
---
# <a name="using-mapi-objects"></a>Uso de objetos MAPI

**Hace referencia a**: Outlook 
  
Los clientes y proveedores de servicios de utilizan objetos MAPI mediante una llamada a los métodos en sus implementaciones de interfaz. Esta es la única forma de que se pueden usar objetos MAPI; métodos que se implementan mediante un objeto fuera de una interfaz de MAPI no son accesibles públicamente. Debido a que todas las interfaces de un objeto están relacionados a través de herencia, usuario de un objeto puede llamar a los métodos en la interfaz base o uno de las interfaces heredadas como si éstos pertenecen a la misma interfaz. 
  
Cuando el usuario de un objeto desea realizar una llamada a un método y ese objeto implementa varias interfaces relacionadas con a través de herencia, el usuario no necesita saber a qué interfaz pertenece el método. El usuario puede llamar a cualquiera de los métodos en cualquiera de las interfaces con un único puntero al objeto. Por ejemplo, en la siguiente ilustración se muestra cómo una aplicación cliente usa un objeto folder. Objetos de carpeta implementan el [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interfaz, que se deriva de [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indirectamente a través [IMAPIProp: IUnknown](imapipropiunknown.md) y [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). Un cliente puede llamar a uno de los métodos **IMAPIProp** , como [IMAPIProp::GetProps](imapiprop-getprops.md)y uno de los [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) métodos, como [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), de la misma manera con el mismo puntero de objeto. Un cliente no es tener en cuenta o afectado por el hecho de que pertenecen estas llamadas a las interfaces diferentes.
  
**Uso de cliente de un objeto de carpeta**
  
![Usar el cliente de un objeto de carpeta] (media/amapi_40.gif "Usar el cliente de un objeto de carpeta")
  
Estas llamadas se traducen en código de manera diferente dependiendo de si el cliente que realiza las llamadas se escribe en C o C++. Antes de hacer cualquier llamada a un método, se debe recuperar un puntero a la implementación de la interfaz. Punteros de interfaz pueden obtenerse de las maneras siguientes:
  
- Llamar a un método en un objeto diferente.
    
- Llamar a una función de la API.
    
- Llamar al método [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) en el objeto de destino. 
    
MAPI proporciona varios métodos y funciones de la API que devuelven punteros a las implementaciones de interfaz. Por ejemplo, los clientes pueden llamar al método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para recuperar un puntero a un objeto table que proporciona acceso a información del proveedor de almacén de mensajes a través de la [IMAPITable: IUnknown](imapitableiunknown.md) interfaz. Proveedores de servicios pueden llamar a la función API [CreateTable](createtable.md) para recuperar un puntero a un objeto de datos de tabla. Cuando no hay ninguna función o método disponibles y los clientes o proveedores de servicio ya tienen un puntero a un objeto, puede llamar al método **QueryInterface** del objeto para recuperar un puntero a otra de las implementaciones de interfaz del objeto. 
  
## <a name="see-also"></a>Vea también

- [Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

