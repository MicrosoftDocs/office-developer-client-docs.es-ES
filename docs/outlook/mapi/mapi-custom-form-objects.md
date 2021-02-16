---
title: Objetos de formulario personalizados MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318252"
---
# <a name="mapi-custom-form-objects"></a>Objetos de formulario personalizados MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los objetos para formularios personalizados se implementan mediante tres componentes diferentes:
  
- Un servidor de formularios.
    
- Un proveedor de bibliotecas de formularios.
    
- Un visor de formularios.
    
Un servidor de formulario tiene una funcionalidad similar a una aplicación de objeto de documento compuesto OLE. Es un componente ejecutable que implementa el formulario; controla su presentación y las operaciones que un usuario puede realizar. MAPI inicia un servidor de formulario cuando se solicita cuando un usuario desea ver un mensaje junto con una clase de mensaje que se muestra mediante un formulario admitido por el servidor de formularios. Los servidores de formulario implementan tres objetos: un objeto de fábrica de formularios similar a la fábrica de clases OLE estándar, un receptor de avisos de formulario para controlar eventos específicos del formulario y el propio formulario. 
  
Un proveedor de bibliotecas de formularios proporciona acceso a los clientes al conjunto de propiedades de un formulario, a su contenedor y al objeto que vincula los mensajes de una clase específica al servidor que puede abrir el formulario para esa clase. Los proveedores de bibliotecas de formularios implementan tres objetos: un objeto de información de formulario, un contenedor de formularios y un administrador de formularios para enlazar un mensaje al servidor de formulario adecuado en función de la clase del mensaje.
  
Un visor de formularios es un componente que se incluye en los clientes que admiten la presentación de formularios personalizados en sus visores de carpetas. Los visores de formularios no son componentes MAPI independientes, al igual que los proveedores de bibliotecas de formularios y los servidores de formulario. Los visores de formularios inician servidores de formulario y proporcionan contexto para ellos. Los visores de formularios implementan tres objetos: un sitio de mensajes, un contexto de vista y un receptor de avisos para controlar eventos específicos de la vista.
  
En la tabla siguiente se describen todos los objetos de formulario personalizados. 
  
|**Form (objeto)**|**Descripción**|
|:-----|:-----|
|Form  <br/> |Controla la presentación y el funcionamiento de un formulario personalizado para ver los mensajes de una clase específica.  <br/> |
|Receptor de avisos de formulario  <br/> |Controla las notificaciones del visor de formularios.  <br/> |
|Fábrica de formularios  <br/> |Crea una instancia de un formulario y permite que su servidor permanezca en la memoria.  <br/> |
|Contenedor de formularios  <br/> |Contiene información del formulario.  <br/> |
|Información del formulario  <br/> |Contiene mensajes y otros contenedores de mensajes.  <br/> |
|Administrador de formulario  <br/> |Proporciona acceso a una vista integrada de la información de formulario personalizada relacionada con todos los formularios instalados. También encuentra las clases de mensajes con los identificadores de clase de formulario correspondientes.  <br/> |
|Sitio de mensajes  <br/> |Controla la manipulación de objetos de formulario desde dentro del cliente y proporciona acceso a un objeto del administrador de formularios.  <br/> |
|Ver contexto  <br/> |Admite comandos de formulario para activar los mensajes siguientes y anteriores y para guardar o imprimir.  <br/> |
|Receptor de avisos de vista  <br/> |Controla las notificaciones del servidor de formularios.  <br/> |
   
En la siguiente ilustración se muestra la relación entre los componentes de formulario personalizados, los objetos e interfaces que implementan y los componentes que son usuarios de los objetos. Tenga en cuenta que, a diferencia de la mayoría de los demás objetos MAPI, el objeto de formulario implementa dos interfaces que no están relacionadas con la herencia directa. Cuando un objeto expone varias interfaces independientes, un usuario del objeto que tiene un puntero a una de las interfaces puede recuperar un puntero a cualquiera de las otras interfaces. Esta capacidad para navegar entre las implementaciones de la interfaz de un objeto es una característica del método [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) 
  
**Componentes de formulario personalizado**
  
![Componentes de formulario personalizados Componentes](media/amapi_67.gif "de formulario personalizados")
  
## <a name="see-also"></a>Consulte también

- [Información general sobre el objeto MAPI y la interfaz](mapi-object-and-interface-overview.md)

