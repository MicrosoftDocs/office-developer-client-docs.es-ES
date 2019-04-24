---
title: Objetos de formulario personalizado MAPI
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
# <a name="mapi-custom-form-objects"></a>Objetos de formulario personalizado MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los objetos de los formularios personalizados se implementan mediante tres componentes diferentes:
  
- Un servidor de formularios.
    
- Un proveedor de bibliotecas de formularios.
    
- Un visor de formulario.
    
Un servidor de formularios es similar en funcionalidad a una aplicación de objeto de documento compuesto OLE. Se trata de un componente ejecutable que implementa el formulario; controla su visualización y las operaciones que puede realizar un usuario. MAPI inicia un servidor de formulario cuando lo solicita cuando un usuario desea ver un mensaje junto con una clase de mensaje que se muestra usando un formulario compatible con el servidor de formularios. Los servidores de formularios implementan tres objetos: un objeto de generador de formularios que se asemeja al generador de clases OLE estándar, un formulario aconsejar a Sink para controlar eventos específicos del formulario y el formulario en sí. 
  
Un proveedor de bibliotecas de formularios proporciona acceso para los clientes a un conjunto de propiedades de un formulario, a su contenedor y al objeto que vincula los mensajes de una clase específica al servidor que puede abrir el formulario para esa clase. Los proveedores de bibliotecas de formularios implementan tres objetos: un objeto de información de formulario, un contenedor de formulario y un administrador de formulario para enlazar un mensaje al servidor de formulario adecuado en función de la clase del mensaje.
  
Un visor de formularios es un componente que se incluye en clientes que admiten la visualización de formularios personalizados en sus visores de carpetas. Los visores de formularios no son componentes MAPI independientes, al igual que los servidores de formularios y los proveedores de bibliotecas de formularios. Los visores de formulario inician servidores de formularios y proporcionan contexto para ellos. Los visores de formularios implementan tres objetos: un sitio de mensajes, un contexto de vista y un receptor de notificaciones para controlar eventos específicos de la vista.
  
En la tabla siguiente se describen todos los objetos de formulario personalizados. 
  
|**Form (objeto)**|**Descripción**|
|:-----|:-----|
|Formulario  <br/> |Controla la presentación y el funcionamiento de un formulario personalizado para ver los mensajes de una clase específica.  <br/> |
|Notificar al receptor de formulario  <br/> |Controla las notificaciones desde el visor de formularios.  <br/> |
|Generador de formularios  <br/> |Crea una instancia de un formulario y permite que su servidor permanezca en la memoria.  <br/> |
|Contenedor de formulario  <br/> |Contiene información del formulario.  <br/> |
|Información de formulario  <br/> |Contiene mensajes y otros contenedores de mensajes.  <br/> |
|Administrador de formulario  <br/> |Proporciona acceso a una vista integrada de información de formulario personalizado relacionada con todos los formularios instalados. También coincide con las clases de mensaje con los identificadores de clase de formulario correspondientes.  <br/> |
|Sitio de mensajes  <br/> |Controla la manipulación de objetos de formulario desde dentro del cliente y proporciona acceso a un objeto de administrador de formularios.  <br/> |
|Contexto de la vista  <br/> |Admite comandos de formulario para activar los mensajes siguientes y anteriores, y para guardar o imprimir.  <br/> |
|Ver el receptor de notificaciones  <br/> |Controla las notificaciones del servidor de formularios.  <br/> |
   
En la siguiente ilustración se muestra la relación entre los componentes de formulario personalizados, los objetos y las interfaces que implementan, y los componentes que son usuarios de los objetos. Observe que, a diferencia de la mayoría de los demás objetos MAPI, el objeto Form implementa dos interfaces que no están relacionadas por la herencia directa. Cuando un objeto expone varias interfaces independientes, un usuario del objeto que tiene un puntero a una de las interfaces puede recuperar un puntero a cualquiera de las demás interfaces. Esta capacidad de navegar entre las implementaciones de interfaz de un objeto es una característica del método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . 
  
**Componentes de formulario personalizado**
  
![Componentes de formularios personalizados] (media/amapi_67.gif "Componentes de formularios personalizados")
  
## <a name="see-also"></a>Vea también

- [Introducción a la interfaz y el objeto MAPI](mapi-object-and-interface-overview.md)

