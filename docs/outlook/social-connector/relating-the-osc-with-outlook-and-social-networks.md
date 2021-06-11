---
title: Información relativa a la OSC con Outlook y las redes sociales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: El Outlook Social Connector (OSC) puede mostrarse en las actividades de la tarjeta de contacto de Office y el panel de personas de Outlook, el estado o las actualizaciones de fotos de un compañero de trabajo, un amigo o cualquier persona con la que esté asociado.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428014"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Información relativa a la OSC con Outlook y las redes sociales

El Outlook Social Connector (OSC) puede mostrarse en las actividades de la tarjeta de contacto de Office y el panel de personas de Outlook, el estado o las actualizaciones de fotos de un compañero de trabajo, un amigo o cualquier persona con la que esté asociado. De forma predeterminada, el OSC muestra Outlook correos electrónicos, datos adjuntos y solicitudes de reunión recibidas de una persona seleccionada. Si la persona seleccionada y el usuario Office colaboran en un sitio de SharePoint, el OSC también muestra actualizaciones de documentos y otras actividades del sitio de SharePoint sitio. Según los contextos de asociación en los que esté interesado el usuario de Office, el usuario de Office puede instalar proveedores de OSC para aplicaciones de línea de negocio, sitios web corporativos internos o una variedad de sitios de redes sociales y profesionales, como LinkedIn, Facebook y Windows Live.
  
Para admitir el uso compartido de funcionalidad en las aplicaciones cliente de Office, el motor principal de OSC se implementa como parte de un componente compartido de Office y el panel de personas se implementa como un complemento Outlook usuario. Para usar el OSC, un usuario de Office debe haber instalado Outlook en ese equipo cliente y configurado Outlook con un perfil, para que el OSC pueda almacenar en caché los contactos de una carpeta Contactos. 
  
Un proveedor de OSC es un DLL del Modelo de objetos componentes (COM) que permite al OSC obtener acceso a los datos de redes sociales de forma independiente de las API de cada red social. Un DLL de proveedor de OSC debe instalarse localmente en un equipo cliente. El proveedor de OSC de una red social conecta el OSC, que forma parte de Outlook, con la red social en Internet.
  
Un proveedor de OSC debe implementar un conjunto de interfaces, definidas como parte de la extensibilidad del proveedor de OSC, para comunicarse con el OSC. La extensibilidad del proveedor de OSC está disponible como una plataforma abierta.
  
La arquitectura del proveedor del OSC permite a varios proveedores trabajar con el motor principal de OSC y agregar información social como amigos y actividades. La figura 1 ilustra la arquitectura del proveedor de OSC.
  
**Figura 1. Outlook Arquitectura del proveedor de Social Connector**

![Redes sociales, proveedores de OSC, OSC y Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminología

En esta Outlook de proveedor de Social Connector, se usa una red social para hacer referencia a los siguientes tipos de sitios: 
  
- Sitios de colaboración como SharePoint.
    
- Sitios de redes sociales como Facebook y Windows Live.
    
- Professional sitios de red como LinkedIn.
    
- Otras aplicaciones de línea de negocio o sitios web internos corporativos usados para redes.
    
El término friend se usa generalmente para incluir amigos, familiares, compañeros, conexiones y cualquier otra persona con la que un usuario de Office esté asociado en un contexto de colaboración como SharePoint o haya agregado a la cuenta de red social del usuario. Los que no son amigos son personas a las que se hace referencia en las actualizaciones de actividad de los amigos, pero no son amigos que se han agregado a la cuenta de red social del usuario Office usuario. Los contactos son personas de una Outlook de contactos. 
  
## <a name="see-also"></a>Vea también

- [Introducción al desarrollo de un Outlook social connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

