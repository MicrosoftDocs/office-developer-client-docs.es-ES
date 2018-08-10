---
title: Información relativa a la OSC con Outlook y las redes sociales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y panel de personas de Outlook actividades, estado o actualizaciones de fotografías para cualquier persona que está asociados con, amigo o un compañero de trabajo.
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821216"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Información relativa a la OSC con Outlook y las redes sociales

Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y panel de personas de Outlook actividades, estado o actualizaciones de fotografías para cualquier persona que está asociados con, amigo o un compañero de trabajo. De forma predeterminada, el OSC muestra los correos electrónicos de Outlook, los datos adjuntos, y las convocatorias de reunión reciben de una persona seleccionada. Si la persona seleccionada y el usuario de Office colaboran en un sitio de SharePoint, el OSC muestra también actualizaciones de documentos y otras actividades de sitio de ese sitio de SharePoint. Dependiendo de los contextos de asociación que es de interés para el usuario de Office, el usuario de Office puede instalar a proveedores de OSC para aplicaciones de línea de negocio, sitios Web corporativos interno o una variedad de sitios de red profesionales y sociales, como LinkedIn, Facebook y Windows Live.
  
Para admitir el uso compartido de la funcionalidad a través de aplicaciones cliente de Office, el motor de núcleo OSC se implementa como parte de un componente compartido de Office y el panel de personas se implementa como un complemento de Outlook. Para usar el OSC, un usuario de Office debe tener instalado Outlook en el equipo cliente y configurar Outlook con un perfil, de modo que el OSC puede almacenar en caché los contactos en una carpeta de contactos. 
  
Un proveedor de OSC es un archivo DLL que permite el OSC tener acceso a datos de redes sociales de una forma que es independiente de la API de cada red social del modelo de objetos de componentes (COM). Un proveedor de OSC DLL debe instalarse localmente en un equipo cliente. Proveedor de OSC de una red social conecta el OSC, que es parte de Outlook, con las redes sociales en Internet.
  
Un proveedor de OSC debe implementar un conjunto de interfaces, definido como parte de la extensibilidad del proveedor OSC, para comunicarse con el OSC. Extensibilidad de proveedores OSC está disponible como una plataforma abierta.
  
La arquitectura de proveedor de la OSC permite varios proveedores para que funcione con el motor de núcleo OSC y agregar información sociales, como amigos y actividades. En la figura 1 ilustra la arquitectura de proveedor OSC.
  
**En la figura 1. Arquitectura de proveedor de Outlook Social Connector**

![Redes sociales, proveedores de OSC, OSC y Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminología

En esta referencia de proveedor de conector de Outlook Social, una red social se utiliza para hacer referencia a los siguientes tipos de sitios: 
  
- Sitios de colaboración, como SharePoint.
    
- Sitios de redes sociales como Facebook y Windows Live.
    
- Sitios de red profesionales, como LinkedIn.
    
- Otras aplicaciones de línea de negocio o sitios Web corporativos internos utilizados redes.
    
El amigo términos se usa generalmente para incluir amigos, familiares, compañeros de trabajo, las conexiones y cualquier otra persona está asociada con en un contexto de colaboración como SharePoint un usuario de Office, o ha agregado a la cuenta de usuario red social. No amigos son las personas que se hace referencia en las actualizaciones de actividad de amigos pero no amigos que se han agregado a la cuenta de red social del usuario de Office. Los contactos son personas en una carpeta de contactos de Outlook. 
  
## <a name="see-also"></a>Vea también

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

