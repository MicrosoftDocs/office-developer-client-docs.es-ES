---
title: Escribir código de servidor de formulario
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
# <a name="writing-form-server-code"></a>Escribir código de servidor de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Puede pensar en un servidor de formularios como el siguiente: 
  
- Un programa Win32 que muestra una interfaz y controla los mensajes de Windows mediante los mecanismos estándar del bombeo de mensajes de Windows.
    
- Un objeto que registra su generador de clases con OLE y se activa mediante los métodos de automatización OLE.
    
- Un objeto MAPI que sigue las reglas MAPI para las interacciones con otros componentes de MAPI.
    
 El código tiene que administrar los tres requisitos generales de forma simultánea. 
  
Vea la sección servicios de objetos COM y ActiveX en el SDK de Windows para obtener detalles sobre cómo registrar el generador de clases de su servidor de formularios. Controlar los mensajes de Windows y mostrar una interfaz son técnicas de programación estándar de Windows que no tienen ningún requisito especial con respecto a los formularios MAPI. De nuevo, el SDK de Windows tiene detalles sobre la programación de Windows. Este documento contiene lo que necesita saber para implementar las interfaces de formulario MAPI necesarias y opcionales para que sigan las reglas MAPI de interacciones con otros componentes MAPI, principalmente las aplicaciones cliente de mensajería y el administrador de formularios MAPI.
  
Todas las interfaces que se pueden usar al implementar servidores de formularios se derivan, ya sea directa o indirectamente, de la clase base [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx). Esto significa que todas las implementaciones de estas interfaces deberán tener métodos **QueryInterface**, **AddRef**y **Release** . Puede ahorrar mucho trabajo si usa varias herencias para implementar todas las interfaces necesarias en una clase nueva, de modo que todas las interfaces que use puedan compartir una única implementación de los métodos **IUnknown** necesarios. Para obtener más información, vea los métodos [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) . No hay ninguna consideración especial con respecto a los servidores de formularios MAPI para estos métodos. 
  
Aunque no todas las interfaces de formulario de MAPI son obligatorias para todos los servidores de formularios, los métodos de una interfaz dada son obligatorios. Es decir, si decide implementar una interfaz determinada, debe implementar todos los métodos en la interfaz. Esto es diferente de la situación con otros componentes MAPI, como los transportes de mensajes. Afortunadamente, los métodos de las interfaces de formulario de MAPI son relativamente sencillos, por lo que la implementación de todos ellos no supone una gran carga para los desarrolladores.
  
Las interfaces de formulario MAPI son independientes del tipo de herramienta de desarrollo que se usa para crear un servidor de formularios. Esto permite que los formularios se creen usando distintas herramientas de desarrollo. El único requisito es que todos los servidores de formulario deben admitir las interfaces de formulario MAPI necesarias.
  
Todos los servidores de formularios requieren todas las interfaces MAPI que están relacionadas con los formularios. Las interfaces opcionales le permiten implementar algunas funciones de formulario avanzadas que no son necesarias para la mayoría de los servidores de formulario. En la siguiente tabla se enumeran las interfaces, para qué son y si debe implementarlas.
  
|**Interfaz**|**Descripción**|**Estado**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |La interfaz principal que los clientes usan para cargar servidores de formularios, ejecutar verbos de formulario y cerrar servidores de formularios. También se trata de la interfaz que se deriva del **IUNKNOWN** OLE que se utiliza para informar a otros componentes OLE acerca de las interfaces que implementa un objeto Form.  <br/> |Obligatorio  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Se usa cuando se cargan mensajes en y se guardan mensajes de objetos de formulario.  <br/> |Obligatorio  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Usada por los objetos Form para realizar un seguimiento del estado del cliente de mensajería y saber si el objeto Form es capaz de mostrar el mensaje siguiente o anterior en una carpeta.  <br/> |Opcional  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |La interfaz de la fábrica de clases OLE usada por los objetos Form para el cumplimiento del mecanismo de factoría de clases OLE.  <br/> |Obligatorio  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Se usa si el servidor de formularios admite más de un tipo de formulario. En este caso, la interfaz **IMAPIFormFactory** permite a las aplicaciones cliente tener acceso a varias interfaces **IClassFactory** (una por cada tipo de formulario que admita su servidor de formularios) que también debe implementar su servidor de formularios.  <br/> |Opcional  <br/> |
   
## <a name="see-also"></a>Vea también



[Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

