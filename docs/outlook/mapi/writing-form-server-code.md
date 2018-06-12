---
title: Escritura de código de servidor de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 860b0150fd1ec66fa8fee387d8d4a96e8bb79761
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820986"
---
# <a name="writing-form-server-code"></a>Escritura de código de servidor de formulario

  
  
**Se aplica a**: Outlook 
  
Puede considerar un servidor de formulario como el siguiente: 
  
- Un programa Win32 que muestra una interfaz y se encarga de los mensajes de windows mediante los mecanismos de suministro de mensajes de Windows estándares.
    
- Un objeto que registra el generador de clases con OLE y se activa por métodos de automatización OLE.
    
- Un objeto MAPI que sigue las reglas MAPI para las interacciones con otros componentes MAPI.
    
 El código tiene que controlar las tres de esos requisitos amplia simultáneamente. 
  
Vea la sección Servicios de objeto de ActiveX y COM en el SDK de Windows para obtener información detallada acerca de cómo registrar el generador de clases del servidor de su formulario. Tratamiento de mensajes de windows y mostrar una interfaz son estándares técnicas de programación de Windows que no tengan requisitos especiales con respecto a los formularios MAPI. Una vez más, el SDK de Windows con información detallada acerca de las ventanas de programación. Este documento contiene lo que necesita saber para implementar las interfaces de formulario MAPI opcionales y obligatorios para que cumplan las reglas MAPI para las interacciones con otros componentes MAPI: principalmente la MAPI de formulario manager y aplicaciones cliente de mensajería.
  
Todas las interfaces que se pueden usar al implementar los servidores de formulario se derivan, directa o indirectamente, de OLE [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)de la clase base. Esto significa que todas las implementaciones de estas interfaces tendrá que tienen métodos **QueryInterface**, **AddRef**y **Release** . Se puede ahorrar una gran cantidad de trabajo si utiliza herencia múltiple para implementar todas las interfaces necesarias en una nueva clase de su elección, de forma que todas las interfaces que use pueden compartir una única implementación de los métodos de **IUnknown** necesarios. Para obtener más información, vea los métodos de [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx), [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)e [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) . No hay ninguna consideración especial con respecto a los servidores de formulario MAPI para estos métodos. 
  
Mientras no todas las interfaces de formulario MAPI son obligatorios para todos los servidores de formulario, los métodos de cualquier interfaz determinado son obligatorios. Es decir, si decide implementar una interfaz determinada, debe implementar todos los métodos en la interfaz. Esto es diferente de la situación con algunos otros componentes MAPI, como los transportes de mensaje. Afortunadamente, los métodos de las interfaces de formulario MAPI son relativamente sencillos, por lo que la implementación de todos ellos no colocar una gran carga en los desarrolladores.
  
Las interfaces de formulario MAPI son independientes del tipo de herramienta de desarrollo que se usa para crear un servidor de formulario. Esto permite que los formularios que se creará mediante las herramientas de desarrollo diferentes. El único requisito es que todos los servidores de formulario deben admitir las interfaces necesarias de formulario MAPI.
  
No todas las interfaces MAPI que se relacionan con formularios son necesarios para todos los servidores de formulario. Las interfaces opcionales permiten implementar algunas funciones avanzadas de formulario que no son necesarios por la mayoría de los servidores de formulario. En la siguiente tabla se enumera las interfaces, ¿qué son y si se debe implementar.
  
|**Interfaz**|**Descripción**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm: IUnknown](imapiformiunknown.md) <br/> |La interfaz principal que utilizan los clientes para cargar los servidores de formulario, ejecutar verbos de formulario y apagar servidores de formulario. También es la interfaz que se deriva el OLE **IUnknown** que se usa para informar a otros componentes OLE con respecto a qué interfaces implementa un objeto de formulario.  <br/> |Obligatorio  <br/> |
|[IPersistMessage: IUnknown](ipersistmessageiunknown.md) <br/> |Se utiliza cuando se cargan los mensajes en y guardar los mensajes de los objetos de formulario.  <br/> |Obligatorio  <br/> |
|[IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) <br/> |Utilizar objetos de formulario para realizar un seguimiento de estado de cliente de mensajería y para averiguar si el objeto de formulario es capaz de mostrar el mensaje siguiente o anterior en una carpeta.  <br/> |Opcional  <br/> |
|[IClassFactory](http://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |La interfaz de fábrica de clase OLE utilizada por los objetos de formulario para el cumplimiento con el mecanismo de fábrica de clase OLE.  <br/> |Obligatorio  <br/> |
|[IMAPIFormFactory: IUnknown](imapiformfactoryiunknown.md) <br/> |Se usa si su servidor de formulario es compatible con más de un tipo de formulario. En este caso, la interfaz de **IMAPIFormFactory** permite a las aplicaciones de cliente para tener acceso a las interfaces **IClassFactory** varias (uno por cada tipo de formulario compatible con el servidor de formulario) que también debe implementar el servidor de formulario.  <br/> |Opcional  <br/> |
   
## <a name="see-also"></a>Ver también



[Desarrollo de los servidores de formulario MAPI](developing-mapi-form-servers.md)

