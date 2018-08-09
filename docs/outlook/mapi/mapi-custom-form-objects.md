---
title: 'MAPI: objetos de formulario personalizado'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ecb40262959834ec511601ec3176887c919d944f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818100"
---
# <a name="mapi-custom-form-objects"></a>MAPI: objetos de formulario personalizado
  
**Hace referencia a**: Outlook 
  
Objetos de los formularios personalizados se implementan mediante tres componentes distintos:
  
- Un servidor de formulario.
    
- Un proveedor de biblioteca de formulario.
    
- Visor de un formulario.
    
Un servidor de formulario es una funcionalidad similar a una aplicación de objetos de documento compuesto OLE. Es un componente ejecutable que implementa el formulario; controla su presentación y las operaciones que puede realizar un usuario. MAPI inicia un servidor de formulario a petición cuando un usuario desea ver un mensaje junto con una clase de mensaje que se muestra mediante el uso de un formulario compatible con el servidor de formulario. Servidores de formulario implementan tres objetos: un objeto de fábrica de formulario que se parece a la OLE estándar de clase de fábrica, un formulario de aviso receptor para controlar los eventos específicos de formulario y el propio formulario. 
  
Un proveedor de la biblioteca de formularios proporciona acceso para los clientes de conjunto de propiedades de un formulario, su contenedor y el objeto que vincula los mensajes de una clase específica en el servidor que puede abrir el formulario para esa clase. Proveedores de biblioteca de formulario implementan tres objetos: un objeto de información de formulario, un contenedor de formulario y un administrador de formulario para enlazar un mensaje en el servidor de forma adecuada en función de la clase del mensaje.
  
Un visor de formulario es un componente que se incluye en los clientes que admiten la presentación de los formularios personalizados en sus visores de carpeta. Visores de formulario no son componentes independientes de MAPI, como son los proveedores de biblioteca de formulario y los servidores de formulario. Visores de formulario iniciarán servidores de formulario y proporcionan contexto para ellos. Visores de formulario implementan tres objetos: un sitio de mensaje, un contexto de vista y un receptor de notificaciones para controlar los eventos específicos de la vista.
  
En la siguiente tabla se describe todos los objetos de formulario personalizado. 
  
|**Objeto de formulario**|**Descripción**|
|:-----|:-----|
|Form  <br/> |Controla la presentación y el funcionamiento de un formulario personalizado para la visualización de los mensajes de una clase específica.  <br/> |
|Formulario de aviso receptor  <br/> |Controla las notificaciones desde el Visor de formulario.  <br/> |
|Generador de formulario  <br/> |Crea una instancia de un formulario y permite que su servidor permanecen en la memoria.  <br/> |
|Contenedor de formulario  <br/> |Contiene información del formulario.  <br/> |
|Información del formulario  <br/> |Contiene los mensajes y otros contenedores de mensaje.  <br/> |
|Administrador de formularios  <br/> |Proporciona acceso a una vista integrada de la información de formulario personalizado que está relacionada con todos los formularios instalados. También coincide con las clases de mensajes con los identificadores de clase de formulario correspondiente.  <br/> |
|Sitio de mensaje  <br/> |Administra la manipulación de objetos de formulario desde dentro del cliente y proporciona acceso a un objeto de administrador de formulario.  <br/> |
|Contexto de vista  <br/> |Admite comandos para activar los mensajes anteriores y siguiente y para guardar o imprimir del formulario.  <br/> |
|Vista de aviso receptor  <br/> |Controla las notificaciones desde el servidor de formulario.  <br/> |
   
En la siguiente ilustración se muestra la relación entre los componentes de formularios personalizados, los objetos y las interfaces que implementan y los componentes que son los usuarios de los objetos. Tenga en cuenta que, a diferencia de la mayoría de objetos MAPI, el objeto de formulario implementa dos interfaces que no están relacionadas por herencia directa. Cuando un objeto expone varias interfaces independientes, un usuario del objeto que tiene un puntero a una de las interfaces puede recuperar un puntero a cualquiera de las otras interfaces. Esta capacidad para navegar entre las implementaciones de interfaz de un objeto es una característica del método [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . 
  
**Componentes de formulario personalizado**
  
![Componentes de formulario personalizado] (media/amapi_67.gif "Componentes de formulario personalizado")
  
## <a name="see-also"></a>Vea también

- [Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

