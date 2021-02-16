---
title: Escritura de código de servidor de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a93e53261d56e452f38e38da427585cecccba405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325798"
---
# <a name="writing-form-server-code"></a>Escritura de código de servidor de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Puede pensar en un servidor de formularios de la siguiente manera: 
  
- Un programa Win32 que muestra una interfaz y controla los mensajes de Windows a través de los mecanismos estándar de mecanismo de bloqueo de mensajes de Windows.
    
- Objeto que registra su fábrica de clases con OLE y se activa mediante métodos de automatización OLE.
    
- Un objeto MAPI que sigue las reglas MAPI para las interacciones con otros componentes MAPI.
    
 El código debe controlar los tres requisitos generales simultáneamente. 
  
Consulta la sección COM y ActiveX Object Services en Windows SDK para obtener más información sobre cómo registrar la fábrica de clases del servidor de formularios. Controlar los mensajes de Windows y mostrar una interfaz son técnicas de programación estándar de Windows que no tienen requisitos especiales con respecto a los formularios MAPI. De nuevo, Windows SDK tiene detalles sobre la programación de Windows. Este documento contiene lo que necesita saber para implementar las interfaces de formulario MAPI obligatorias y opcionales para que sigan las reglas MAPI para las interacciones con otros componentes MAPI, principalmente el administrador de formularios MAPI y las aplicaciones cliente de mensajería.
  
Todas las interfaces que puede usar al implementar servidores de formulario se derivan, directa o indirectamente, de la clase base [OLE IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx). Esto significa que todas las implementaciones de estas interfaces tendrán que tener los métodos **QueryInterface**, **AddRef** **y Release.** Puede ahorrarse mucho trabajo si usa varias herencias para implementar todas las interfaces necesarias en una nueva clase propia, de modo que todas las interfaces que use puedan compartir una sola implementación de los métodos **IUnknown** necesarios. Para obtener más información, vea los métodos [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)e [IUnknown::Release.](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) No hay consideraciones especiales con respecto a los servidores de formulario MAPI para estos métodos. 
  
Aunque no todas las interfaces de formulario MAPI son obligatorias para todos los servidores de formulario, los métodos de una interfaz determinada son obligatorios. Es decir, si decide implementar una interfaz determinada, debe implementar todos los métodos de la interfaz. Esto es diferente de la situación con algunos otros componentes MAPI, como los transportes de mensajes. Afortunadamente, los métodos de las interfaces de formulario MAPI son relativamente sencillos, por lo que implementarlos todos no supone una gran carga para los desarrolladores.
  
Las interfaces de formulario MAPI son independientes del tipo de herramienta de desarrollo que se usa para crear un servidor de formularios. Esto permite crear formularios con diferentes herramientas de desarrollo. El único requisito es que todos los servidores de formularios deben admitir las interfaces de formulario MAPI necesarias.
  
No todas las interfaces MAPI relacionadas con formularios son necesarias para todos los servidores de formularios. Las interfaces opcionales permiten implementar algunas funciones de formulario avanzadas que no son necesarias para la mayoría de los servidores de formulario. En la tabla siguiente se enumeran las interfaces, para qué están y si se deben implementar.
  
|**Interfaz**|**Descripción**|**Estado**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |La interfaz principal que los clientes usan para cargar servidores de formulario, ejecutar verbos de formulario y apagar servidores de formulario. También es la interfaz derivada de OLE **IUnknown** que se usa para informar a otros componentes OLE sobre las interfaces que implementa un objeto de formulario.  <br/> |Obligatorio  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Se usa al cargar y guardar mensajes desde objetos de formulario.  <br/> |Obligatorio  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Los objetos de formulario lo usan para realizar un seguimiento del estado del cliente de mensajería y para averiguar si el objeto de formulario es capaz de mostrar el mensaje siguiente o anterior en una carpeta.  <br/> |Opcional  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |La interfaz de fábrica de clases OLE que usan los objetos de formulario para cumplir con el mecanismo de fábrica de clase OLE.  <br/> |Obligatorio  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Se usa si el servidor de formulario admite más de un tipo de formulario. En este caso, la interfaz **IMAPIFormFactory** permite a las aplicaciones cliente tener acceso a varias interfaces **IClassFactory** (una por tipo de formulario compatible con el servidor de formulario) que el servidor de formulario también debe implementar.  <br/> |Opcional  <br/> |
   
## <a name="see-also"></a>Consulte también



[Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md)

