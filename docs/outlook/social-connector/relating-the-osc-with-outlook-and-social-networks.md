---
title: Información relativa a la OSC con Outlook y las redes sociales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y las actividades del panel de personas de Outlook, el estado o las actualizaciones de fotos de un compañero de trabajo, un amigo o cualquier persona con la que esté asociado.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428014"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Información relativa a la OSC con Outlook y las redes sociales

Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y las actividades del panel de personas de Outlook, el estado o las actualizaciones de fotos de un compañero de trabajo, un amigo o cualquier persona con la que esté asociado. De forma predeterminada, el OSC muestra los correos electrónicos, los datos adjuntos y las solicitudes de reunión de Outlook recibidos de una persona seleccionada. Si la persona seleccionada y el usuario de Office colaboran en un sitio de SharePoint, el OSC también muestra actualizaciones de documentos y otras actividades del sitio desde ese sitio de SharePoint. En función de los contextos de asociación que le interesan al usuario de Office, el usuario de Office puede instalar proveedores de OSC para aplicaciones de línea de negocio, sitios web corporativos internos o una variedad de sitios de redes sociales y profesionales, como LinkedIn, Facebook y Windows Live.
  
Para admitir el uso compartido de funciones entre aplicaciones cliente de Office, el motor principal de OSC se implementa como parte de un componente compartido de Office y el panel de personas se implementa como un complemento de Outlook. Para usar el OSC, un usuario de Office debe haber instalado Outlook en ese equipo cliente y configurado Outlook con un perfil, para que el OSC pueda almacenar en caché los contactos de una carpeta Contactos. 
  
Un proveedor de OSC es un ARCHIVO DLL del modelo de objetos componentes (COM) que permite que el OSC acceda a los datos de la red social de forma que sea independiente de las API de cada red social. Una DLL del proveedor de OSC debe instalarse localmente en un equipo cliente. El proveedor de OSC de una red social conecta el OSC, que forma parte de Outlook, con la red social en Internet.
  
Un proveedor de OSC debe implementar un conjunto de interfaces, definidas como parte de la extensibilidad del proveedor de OSC, para comunicarse con el OSC. La extensibilidad del proveedor de OSC está disponible como plataforma abierta.
  
La arquitectura del proveedor del OSC permite a varios proveedores trabajar con el motor principal de OSC y agregar información social como amigos y actividades. La figura 1 ilustra la arquitectura del proveedor de OSC.
  
**Figura 1. Arquitectura de proveedor de Outlook Social Connector**

![Redes sociales, proveedores de OSC, OSC y Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminología

En esta referencia de proveedor de Outlook Social Connector, se usa una red social para hacer referencia a los siguientes tipos de sitios: 
  
- Sitios de colaboración como SharePoint.
    
- Sitios de redes sociales como Facebook y Windows Live.
    
- Sitios de red profesionales como LinkedIn.
    
- Otras aplicaciones de línea de negocio o sitios web internos corporativos usados para las redes.
    
El término friend se usa generalmente para incluir amigos, familiares, compañeros, conexiones y cualquier otra persona con la que un usuario de Office está asociado en un contexto de colaboración como SharePoint, o se ha agregado a la cuenta de red social del usuario. Los que no son amigos son personas a las que se hace referencia en las actualizaciones de actividad de los amigos, pero no son amigos que se han agregado a la cuenta de red social del usuario de Office. Los contactos son personas de una carpeta de contactos de Outlook. 
  
## <a name="see-also"></a>Consulte también

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

